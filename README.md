Stacking	is	an	interesting	approach	to	building	ensemble	models	that	is particularly	effective	when	heterogenous	
mixes	of base	classifiers	is	used.	While	less	commonly	used	than	its	bagging	and	boosting	counterparts,	the	stacked	
ensemble	idea	has	been	around	for	as	long	as	ensemble	models	have	been	popular	in	machine	learning	- 
for	example	(Wolpert,	1992). In	stacked	ensembles	a	set	of base	classifiers	are	trained, and	their	outputs	are	combined	
into	a	training set	for	the	stack layer	classifier.	One	of	the	main	challenges	in	building	effective	stacked	ensembles	
is	designing	the	process	to	generate	the	data	to	train	the	models	at	the	stack	layer.

The	task	in	this	Project	is	to	implement	a	selection	of	stacked	ensemble	approaches.	

1. Create	the	simple Stacked Ensemble Classifier 
2. implement the Stacked Ensemble Classifier Hold Out so	that	it	uses	a	hold-out	test	set	to	
generate	the	stack	training	dataset.
3. Implement the	StackedEnsembleClassifier	implementation	provided	to	create Stacked Ensemble Classifier KFold so	that 
it uses	a	k-fold	cross	validation	approach	to	generate	the	stack	training	dataset (this	essentially implements 
the	SuperLearner	model	described	by	van	der	Laan et	al	(2007)).
4. Compare the	performance	of	the	StackedEnsembleClassifier,StackedEnsembleClassifierHoldOut,	and	StackedEnsembleClassifierkFold	
implementations.	
5. We	can	divide	ensemble	training	algorithms	into	those	that	attempt	to	build	ensembles	of	generalists and	those	that	build	
ensembles	of	specialists.	One	way	to	build	an	ensemble	of	specialists	is	to	build	an	ensemble	of	one-vs-one	models	each	
of	which	only	considers	two	of	the	classes	from	the	overall	dataset.	The	base	layer	in	this	model	will	include	
models,	where	L	is	the	number	of	classes	in	the	classification	problem.	So,	for	example, if	a	problem	has	four	classes,	0	– 3,	it	will	have	
six	binary	base	models	that	distinguish	between	classes	0-1,	0-2,	0-3,	1-2,	1-3,	and	2-3.	The	outputs of	these	models	can	be	combined	using	a	
stacked	layer	model.	Each	of	these	binary	models	should	be	trained	on	only	instances	from	an	
overall	training	dataset	that	have target	levels	relevant	to	that	binary	model.	Implement	a	one-vs-one	stacked	ensemble	algorithm	in	a	class	
called	StackedEnsembleClassifierOneVsOne (this	implementation	is	a	large step	towards	implementing	the	Troika	stacked	ensemble	algorithm,
described	by	Menahem et	al	(2009)).
