x.bin: xmas23.mac
	RT11 MACRO /LIST:xmas23.LST xmas23.mac
	pclink11 /EXECUTE:xmas23.sav xmas23.OBJ
	bash -c "tail -c +523 xmas23.sav | head -c $$((4 + `od -An --skip-bytes=524 -N2 -d xmas23.sav`)) >$@"
