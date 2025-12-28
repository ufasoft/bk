x.bin: xmas25.mac
	RT11 MACRO /LIST:xmas25.LST xmas25.mac
	pclink11 /EXECUTE:xmas25.sav xmas25.OBJ
	bash -c "tail -c +519 xmas25.sav | head -c $$((4 + `od -An --skip-bytes=520 -N2 -d xmas25.sav`)) >$@"
