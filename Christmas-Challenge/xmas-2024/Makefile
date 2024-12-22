x.bin: xmas24.mac
	RT11 MACRO /LIST:xmas24.LST xmas24.mac
	pclink11 /EXECUTE:xmas24.sav xmas24.OBJ
	bash -c "tail -c +517 xmas24.sav | head -c $$((4 + `od -An --skip-bytes=518 -N2 -d xmas24.sav`)) >$@"
