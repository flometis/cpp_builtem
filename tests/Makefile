include ../Makefile.builtem

TARGETS = compile_test

.PHONY: all compile
all: compile
compile: $(call exe,$(TARGETS))

$(call exe,$(TARGETS)): $(call exe,%): $$(call obj,%)
	$(call link_exe,$@,$^,$(call win_subsystem,console))

.PHONY: clean
clean:
	$(call rm,.build $(call all_exe,$(TARGETS)))
