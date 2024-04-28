NAME = megaphone
CC = c++
RM = rm -rf
FLAGS = -Wall -Wextra -Werror -g -pedantic -std=c++98
SRC = megaphone.cpp
OBJ = $(SRC:.cpp=.o)
DEP = $(SRC:.cpp=.d)

all: $(NAME)
%.o: %.c Makefile
	$(CC) -MMD $(FLAGS) -c $< -o $@ $(INC)
$(NAME): $(OBJ)
	$(CC) $(FLAGS) $(OBJ) -o $(NAME)
fclean: clean
	$(RM) $(NAME)
clean:
	$(RM) $(OBJ) $(DEP)
re: fclean all
.PHONY: all clean fclean re
-include $(DEP)