BUILD_DIR   = build
MAIN_FILE   = main.tex
LETTER_FILE = response_letter.tex
MAIN_PDF    = $(BUILD_DIR)/main.pdf

.PHONY: all clean watch

all: main

main: $(MAIN_FILE)
		@mkdir -p $(BUILD_DIR)
		latexmk -pdf -output-directory=$(BUILD_DIR) $(MAIN_FILE)
		cp $(MAIN_PDF) ../
		open $(MAIN_PDF) &

clean:
		latexmk -C
		@rm -rf $(BUILD_DIR)

watch:
		@mkdir -p $(BUILD_DIR)
		latexmk -pdf -output-directory=$(BUILD_DIR) -pvc $(MAIN_FILE)
