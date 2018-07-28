## 6.1 链表
Linux内核实现的链表是一个双向循环链表，结构定义如下：
``` C
struct list_head {
    struct list_head *next;
    struct list_head *prev;
};
```
链表头定义如下：
``` C
#define LIST_HEAD(name) \
	struct list_head name = LIST_HEAD_INIT(name)

static inline void INIT_LIST_HEAD(struct list_head *list)
{
	list->next = list;
	list->prev = list;
}
```
添加一个节点到链表：
``` C++
static inline void list_add(struct list_head *new, struct list_head *head)
{
	__list_add(new, head, head->next);
}
static inline void list_add_tail(struct list_head *new, struct list_head *head)
{
	__list_add(new, head->prev, head);
}
static inline void __list_add(struct list_head *new,
			      struct list_head *prev,
			      struct list_head *next)
{
	next->prev = new;
	new->next = next;
	new->prev = prev;
	prev->next = new;
}
```
`list_add`将节点加到`head`后面，而`list_add_tail`将链表加到`head`前面。  
从链表里面删除一个节点：
``` C
static inline void list_del(struct list_head *entry)
{
	__list_del(entry->prev, entry->next);
	entry->next = LIST_POISON1;
	entry->prev = LIST_POISON2;
}
static inline void __list_del(struct list_head * prev, struct list_head * next)
{
	next->prev = prev;
	prev->next = next;
}
```
掌握基本的操作后，再来看看如何用内核提供给我们的链表，例如我要定义一个学生结构体，每个学生串联起来组成一个链表，可以定义如下：
``` C
struct Student {
    int id;
    char *name;
    int age;
    struct list_head lists;
};

int main() {
    struct Student s1 = {
        .id = 1;
        .name = "Harlon";
        .age = 18;
        .lists = LIST_HEAD_INIT(s1.lists);
    };

    struct Student s2 = {
        .id = 2;
        .name = "Jack";
        .age = 20;
        .lists = LIST_HEAD_INIT(s2.lists);
    };

    static LIST_HEAD(s_list);
    list_add(&s1.lists, s_list);
    list_add(&s2.lists, s_list);
    
    struct Student *s;
    list_for_each_entry(s, &s_list, lists) {
        printf("id: %d, name: %s, age: %d", s->id, s->name, s->age);
    }

    return 0;
}
```
