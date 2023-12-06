NAME = physics_khin_m1.pdf

SRC = khin_m1.tex

GARBAGE_FOLDER = garbage
LOG_FILE = latex_logs

CLR = pdflatex


GREEN = \033[32m
YELLOW = \033[0;33m
RED = \033[0;31m
GRAY = \033[2;37m
CURSIVE = \033[3m
NO_COLOR = \x1b[0m


all: $(NAME)
.PHONY: all

$(NAME): $(SRC) $(GARBAGE_FOLDER) Makefile
	@$(CLR) -jobname=$(basename $(NAME)) $(SRC) > $(GARBAGE_FOLDER)/$(LOG_FILE)
	@printf "\n$(CURSIVE)Assembling $(NAME) ⚙️ ... $(GREEN)DONE! 🥂\n"
	@mv *.log *.aux $(GARBAGE_FOLDER)/

$(GARBAGE_FOLDER):
	@mkdir $(GARBAGE_FOLDER)

clean:
	@rm -rf $(GARBAGE_FOLDER)
.PHONY: clean

fclean: clean
	@rm -rf $(NAME)
.PHONY: fclean

re: fclean all
.PHONY: re

open:
	open $(NAME)
.PHONY: open
