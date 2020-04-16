all: 
	pip install PyQt5

pack:
	del xmarek72_xnepra01_xlukac15.zip
	mkdir xmarek72_xnepra01_xlukac15
	make doc && move doc xmarek72_xnepra01_xlukac15
	mkdir install && move install xmarek72_xnepra01_xlukac15
	git clone https://github.com/kate-nepra/ivs-proj2.git xmarek72_xnepra01_xlukac15/repo
	zip -r xmarek72_xnepra01_xlukac15.zip xmarek72_xnepra01_xlukac15 && rmdir /Q /S xmarek72_xnepra01_xlukac15 

clean:
	rmdir /Q /S __pycache__  || rmdir /Q /S doc 

test:
	python math_lib_test.py

doc:
	mkdir doc
	doxygen Doxyfile 

run:
	python main.py

profile:
	python stddev.py <profiling_example_file.txt

help:	
	@echo make/ make all - install dependencies
	@echo pack           - pack needed files
	@echo make clean     - clean not needed files
	@echo make test      - start tests for math_library
	@echo make doc       - generate documentation wuth Doxygen
	@echo make run       - start program
	@echo make profile   - start code for standard deviation with example file
	@echo make help      - print make info for this program