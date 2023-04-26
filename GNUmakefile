PREFIX = /usr

all:
	$(CC) -fPIC -shared -I$(PWD) -I$(PWD)/elftoolchain-common elf.c elf_begin.c elf_cntl.c elf_end.c elf_errmsg.c elf_errno.c elf_data.c elf_fill.c elf_flag.c elf_getarhdr.c elf_getarsym.c elf_getbase.c elf_getident.c elf_hash.c elf_kind.c elf_memory.c elf_next.c elf_open.c elf_rand.c elf_rawfile.c elf_phnum.c elf_shnum.c elf_shstrndx.c elf_scn.c elf_strptr.c elf_update.c elf_version.c gelf_cap.c gelf_checksum.c gelf_dyn.c gelf_ehdr.c gelf_getclass.c gelf_fsize.c gelf_move.c gelf_phdr.c gelf_rel.c gelf_rela.c gelf_shdr.c gelf_sym.c gelf_syminfo.c gelf_symshndx.c gelf_xlate.c libelf_align.c libelf_allocate.c libelf_ar.c libelf_ar_util.c libelf_checksum.c libelf_data.c libelf_ehdr.c libelf_extended.c libelf_memory.c libelf_open.c libelf_phdr.c libelf_shdr.c libelf_xlate.c libelf_fsize.c libelf_msize.c libelf_convert.c -o libelf.so

clean:
	rm -v libelf.so

install:
	mkdir -pv $(DESTDIR)$(PREFIX)/lib
	cp -v libelf.so $(DESTDIR)$(PREFIX)/lib
	mkdir -pv $(DESTDIR)$(PREFIX)/share/man/man3
	cp -v *.3 $(DESTDIR)$(PREFIX)/share/man/man3
	mkdir -v $(DESTDIR)$(PREFIX)/include
	cp -v libelf.h gelf.h elftoolchain-common/elfdefinitions.h $(DESTDIR)$(PREFIX)/include
