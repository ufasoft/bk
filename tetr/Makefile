MACRO11=RT11 MACRO

tetr.bin: tetr.mac
	$(MACRO11) /LIST:tetr.lst tetr.mac
	pclink11 /EXECUTE:tetr.sav tetr.OBJ
	bash -c "dd if=tetr.sav of=$@ bs=1 skip=508 count=$$((4 + `od -An --skip-bytes=510 -N2 -d tetr.sav`))"
