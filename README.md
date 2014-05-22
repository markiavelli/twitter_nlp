Forked Twitter NLP Tools
========================

Reason to change:
-----------------
This fork runs properly on tweets containing Unicode characters.

-------------------------------

Authors: Alan Ritter, Sam Clark

contact: aritter@cs.washington.edu

Example Usage:
--------------

	export TWITTER_NLP=./
	cat test.1k.txt | python python/ner/extractEntities2.py

note: this takes a minute or so to read in models from files


To include classification, simply add the --classify switch:

	cat test.1k.txt | python python/ner/extractEntities2.py --classify


For higher quality, but slower results, optionally include features based on POS and chunk tags
(chunk tags require POS)

	cat test.1k.txt | python python/ner/extractEntities2.py --classify --pos
	cat test.1k.txt | python python/ner/extractEntities2.py --classify --pos --chunk

Also has the ability to include event tags (requires POS):

	cat test.1k.txt | python python/ner/extractEntities2.py --classify --pos --event
