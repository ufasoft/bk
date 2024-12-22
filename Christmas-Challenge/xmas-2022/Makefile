MACRO11=RT11 MACRO

x.bin: xmas.mac
	$(MACRO11) /LIST:xmas.LST xmas.mac
	pclink11 /EXECUTE:xmas.sav xmas.OBJ
	bash -c "tail -c +527 xmas.sav | head -c $$((4 + `od -An --skip-bytes=528 -N2 -d xmas.sav`)) >$@"
