<div align="center">

# 📚 Libft

_Your very first own library._

[![42 School](https://img.shields.io/badge/42-School-000000?style=for-the-badge&logo=42&logoColor=white)](https://42.fr/)
[![Grade](https://img.shields.io/badge/Grade-125%2F125-success?style=for-the-badge)]()
[![Language](https://img.shields.io/badge/Language-C-blue?style=for-the-badge&logo=c&logoColor=white)]()
[![Norminette](https://img.shields.io/badge/Norminette-Passing-brightgreen?style=for-the-badge)]()

</div>

---

## 📖 About

**Libft** is the first project of the 42 cursus. The goal is to recode a set of standard C library functions from scratch, along with a handful of custom utilities, and package them into a static library (`libft.a`) reusable in every subsequent C project.

> This library is the foundation for all upcoming 42 projects — `ft_printf`, `get_next_line`, `push_swap`, `so_long`, `minishell` and beyond all rely on it.

---

## 🎯 Project scope

- ✅ **Part 1** — Libc functions rewritten from scratch
- ✅ **Part 2** — Additional utility functions
- ✅ **Bonus** — Linked list manipulation toolkit

---

## 🧰 Functions implemented

### Part 1 — Libc rewrites

| Character checks | String manipulation | Memory | Conversions |
|:-:|:-:|:-:|:-:|
| `ft_isalpha` | `ft_strlen`   | `ft_memset`  | `ft_atoi`    |
| `ft_isdigit` | `ft_strlcpy`  | `ft_bzero`   | `ft_toupper` |
| `ft_isalnum` | `ft_strlcat`  | `ft_memcpy`  | `ft_tolower` |
| `ft_isascii` | `ft_strchr`   | `ft_memmove` |              |
| `ft_isprint` | `ft_strrchr`  | `ft_memchr`  |              |
|              | `ft_strncmp`  | `ft_memcmp`  |              |
|              | `ft_strnstr`  | `ft_calloc`  |              |
|              | `ft_strdup`   |              |              |

### Part 2 — Additional functions

| String creation | String utilities | Write to fd |
|:-:|:-:|:-:|
| `ft_substr`  | `ft_striteri` | `ft_putchar_fd` |
| `ft_strjoin` | `ft_strmapi`  | `ft_putstr_fd`  |
| `ft_strtrim` | `ft_itoa`     | `ft_putendl_fd` |
| `ft_split`   |               | `ft_putnbr_fd`  |

### Bonus — Linked lists

| Creation | Traversal | Modification |
|:-:|:-:|:-:|
| `ft_lstnew` | `ft_lstsize` | `ft_lstadd_front` |
|             | `ft_lstlast` | `ft_lstadd_back`  |
|             | `ft_lstiter` | `ft_lstdelone`    |
|             | `ft_lstmap`  | `ft_lstclear`     |

---

## 🛠️ Build

```bash
# Clone
git clone https://github.com/Vavongg/libft.git
cd libft

# Mandatory part
make

# With bonus (linked lists)
make bonus

# Cleanup
make clean    # remove .o files
make fclean   # remove .o files + libft.a
make re       # full rebuild
```

Output: **`libft.a`** — a static library ready to be linked.

---

## 🚀 Usage

Include the header and link the library when compiling your project:

```c
#include "libft.h"

int main(void)
{
    char *str = ft_strdup("Hello, 42!");
    ft_putendl_fd(str, 1);
    free(str);
    return (0);
}
```

```bash
cc main.c -L. -lft -I. -o my_program
```

---

## 📁 Structure

```
libft/
├── Makefile
├── libft.h            # Public header
├── ft_is*.c           # Character classification
├── ft_str*.c          # String functions
├── ft_mem*.c          # Memory functions
├── ft_put*_fd.c       # Output helpers
├── ft_*toa*.c         # Conversions
└── ft_lst*_bonus.c    # Linked list toolkit
```

---

<div align="center">

Built with ☕ at **42 School** · [github.com/Vavongg](https://github.com/Vavongg)

</div>
