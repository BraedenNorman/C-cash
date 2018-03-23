all: tunit punit bunit blocktest

tunit: trnslist.h trnslist.c tlist-test-unit.c
	gcc trnslist.c tlist-test-unit.c -o tunit

punit: puzzle.h puzzle.c puzzle-test-unit.c
	gcc puzzle.c puzzle-test-unit.c sha1/sha1.c -o punit

bunit: puzzle.h puzzle.c trnslist.h trnslist.c block.h block.c block-test-unit.c
	gcc puzzle.c trnslist.c block.c block-test-unit.c sha1/sha1.c -o bunit
	
blocktest: puzzle.h puzzle.c trnslist.h trnslist.c block.h block.c blockchain.h blockchain.c block-chain-test.c
	gcc puzzle.c trnslist.c block.c sha1/sha1.c blockchain.c block-chain-test.c -o blocktest
	

clean:
	@rm -f *.o tunit punit bunit