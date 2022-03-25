
Analysis Description
--------------------
Perform a Fast Unbiased AppRoximate Bayesian (FUBAR) analysis of a
coding sequence alignment to determine whether some sites have been
subject to pervasive purifying or diversifying selection. v2.1
introduces two more methods for estimating the posterior distribution of
grid weights: collapsed Gibbs MCMC (faster) and 0-th order Variation
Bayes approximation (fastest). Please note that a FUBAR analysis
generates a cache and a results JSON file in the same directory as
directory as the original alignment. HyPhy needs to have write
privileges to this directory. For example if the original file is in
/home/sergei/FUBAR/data/pol.nex then at the end of a FUBAR run, there
will also exist FUBAR-generated files
/home/sergei/FUBAR/data/pol.nex.FUBAR.json,
/home/sergei/FUBAR/data/pol.nex.fubrar.cache. They also provide
checkpointing so that a partially completed analysis can be restarted.

- __Requirements__: in-frame codon alignment (possibly partitioned) and a phylogenetic tree
(one per partition)

- __Citation__: FUBAR: a fast, unconstrained bayesian approximation for inferring
selection (2013), Mol Biol Evol. 30(5):1196-205

- __Written by__: Sergei L Kosakovsky Pond

- __Contact Information__: spond@temple.edu

- __Analysis Version__: 2.2


>code –> Universal

-------
>[WARNING] This dataset contains 397 duplicate sequences. Identical
sequences do not contribute any information to the analysis and only
slow down computation. Please consider removing duplicate or 'nearly'
duplicate sequences, e.g. using
https://github.com/veg/hyphy-analyses/tree/master/remove-duplicates
prior to running selection analyses
-------

>Loaded a multiple sequence alignment with **492** sequences, **419** codons, and **1** partitions from `/raid5/glp1/lx/cova/dn-ds/500/BA.1/prots_nmsa/N.msa`
Save FUBAR cache to : 
>cache –> /raid5/glp1/lx/cova/dn-ds/500/BA.1/prots_nmsa/FUBAR/N.FUBAR.cache
> FUBAR will write cache and result files to _/raid5/glp1/lx/cova/dn-ds/500/BA.1/prots_nmsa/N.msa.FUBAR.cache_ and _/raid5/glp1/lx/cova/dn-ds/500/BA.1/prots_nmsa/N.msa.FUBAR.json_, respectively 


> Number of grid points per dimension (total number is D^2) (permissible range = [5,50], default value = 20, integer): 
>grid –> 20

>method –> Variational-Bayes
> The concentration parameter of the Dirichlet prior (permissible range = [0.001,1], default value = 0.5): 
>concentration_parameter –> 0.5

>non-zero –> No


### Obtaining branch lengths and nucleotide substitution biases under the nucleotide GTR model
Error:
The number of tree tips in 'f_XHsyET.tree_0'(3501) is not equal to the number of sequences in the data filter associated with the tree (492).

Function call stack
1 :  LikelihoodFunction f_XHsyET.likelihoodFunction = (qg_ykbxv.lf_components);

-------
2 :  ExecuteCommands(commands, /home/gdy/miniconda3/share/hyphy/TemplateBatchFiles/libv3/);
-------
3 :  [namespace = qg_ykbxv] utility.ExecuteInGlobalNamespace("LikelihoodFunction `lfid` = (`&lf_components`)");
-------
4 :  [namespace = f_XHsyET] df=estimators.CreateLFObject(this_namespace,data_filter,tree,model_template,initial_values,run_options,None);
-------
5 :  [namespace = etTaWJPS] return estimators.FitSingleModel_Ext(data_filter,tree,"models.DNA.GTR.ModelDescription",initial_values,run_options);
-------
6 :  [namespace = YSyUiLRv] return estimators.FitGTR_Ext(data_filter,tree,initial_values,{});
-------
7 :  [namespace = fubar] gtr_results=estimators.FitGTR(filter_names,trees,gtr_results);
-------
8 :  [namespace = fubar] doGTR("fubar");
-------
9 :  namespace 

Step 0.doGTR("fubar");;
-------
