NAME = compiled-app
SRC  = app/main.c

all: $(NAME)

$(NAME): $(SRC)
	gcc -o $(NAME) $(SRC)

clean:
	rm -f $(NAME)

re: clean all

.PHONY: all clean re
