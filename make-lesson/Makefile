#assigns all the dat files to a txt file called results
results.txt : isles.dat abyss.dat last.dat
	python zipf_test.py isles.dat abyss.dat last.dat > results.txt

# Count words. 
isles.dat : books/isles.txt
	python wordcount.py books/isles.txt isles.dat
	
abyss.dat : books/abyss.txt
	python wordcount.py books/abyss.txt abyss.dat
	
last.dat : books/last.txt
	python wordcount.py books/last.txt last.dat

.PHONY : clean	
clean : 
	rm -f *.dat
	rm -f results.txt
	
.PHONY : dats
dats : isles.dat abyss.dat last.dat
	

