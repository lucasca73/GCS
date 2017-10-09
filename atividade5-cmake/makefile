release:
	$(MAKE) clean
	mkdir build
	cd ./build && cmake -DCMAKE_BUILD_TYPE=Release .. && make && ./bestproject

debug:
	$(MAKE) clean
	mkdir build
	cd ./build && cmake -DCMAKE_BUILD_TYPE=Debug .. && make && ./bestproject

clean:
	rm -r -f build
