$(shell mkdir -p ./build)
BUILD_DIR = $(abspath ./build)
TRANSFER = $(BUILD_DIR)/transfer

.DEFAULT_GOAL = app

$(TRANSFER): scripts/transfer.c
	@echo + build $(TRANSFER)
	@$(CC) -o $@ $<

app: $(TRANSFER)
	@bash scripts/gen.sh
	@echo BUILD DONE.

clean:
	@rm -rf $(TRANSFER) $(BUILD_DIR)

.PHONY: app clean
