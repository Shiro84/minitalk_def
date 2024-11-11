# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: matomas <marvin@42.fr>                     +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/10/31 14:17:05 by matomas           #+#    #+#              #
#    Updated: 2024/11/05 15:46:26 by matomas          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = minitalk

LIBFT_PATH = LIBFT_Marc/
LIBFT_LIB = $(LIBFT_PATH)libft.a


DEF_COLOR =		\033[0;39m
GRAY =			\033[0;90m
RED =			\033[0;91m
GREEN =			\033[0;92m
YELLOW =		\033[0;93m
BLUE =			\033[0;94m
MAGENTA =		\033[0;95m
CYAN =			\033[0;96m
WHITE =			\033[0;97m
BLACK =			\033[0;99m
ORANGE =		\033[38;5;209m
BROWN =			\033[38;2;184;143;29m
DARK_GRAY =		\033[38;5;234m
MID_GRAY =		\033[38;5;245m
DARK_GREEN =	\033[38;2;75;179;82m
DARK_YELLOW =	\033[38;5;143m

SRCS = 	server.c client.c
OBJS = $(SRCS:.c=.o)

CC = gcc
RM = rm -f
CFLAGS = -Wall -Wextra -Werror

# **************************************************************************** #
#                                 REGLAS                                       #
# **************************************************************************** #

all: $(LIBFT_LIB) server client

$(LIBFT_LIB):
	@echo "${BLUE}Compilando LIBFT_Marc..${DEF_COLOR}"
	@$(MAKE) -C $(LIBFT_PATH)

server: server.o $(LIBFT_LIB)
	$(CC) $(CFLAGS) server.o -o server -L$(LIBFT_PATH) -lft

client: client.o $(LIBFT_LIB)
	$(CC) $(CFLAGS) client.o -o client -L$(LIBFT_PATH) -lft

clean:
	@$(RM) $(OBJS)
	@$(MAKE) -C $(LIBFT_PATH) clean
	@echo "${RED}Objetosn eliminados${DEF_COLOR}"

fclean: clean
	@$(RM) server client
	@$(MAKE) -C $(LIBFT_PATH) fclean
	@echo "${RED}Limpieza completa${DEF_COLOR}"

re: fclean all

.PHONY: all clean fclean re
