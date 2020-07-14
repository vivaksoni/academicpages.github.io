<h2>Research</h2>

As a population genetecist I am interested in how patterns of genetic diversity vary within and between different populations. It's a great time to be involved in this field. 
Where once geneticists had access to data from a small number of loci, the revolution in next generation sequencing means we have access to whole genome sequence data for 
numerous species. The challenge has shifted from attempting to obtain enough data to generate significant results, to attempting to make sense of the large amount of information 
we now have at our disposal. Principally I am a bioinformatician, attempting to generate insights from this data using the vast amount of computing power that labs have access to.

The fundamental forces of evolution are mutation, genetic drift, gene flow and natural selection. Under the supervision of Adam Eyre-Walker at the University of Sussex, 
I have primarily focussed on developing and utilising methods to detect natural selection in humans using DNA sequence data. I am coming towards the end of what has been an
incredibly rewarding time at Sussex and am on the lookout for post-doc positions in suitable labs. Pre-prints and publications will be available soon.

<br />

<h2>Current Projects</h2>

I will briefly introduce the four projects I have been working on during my PhD. These summaries barely scratch the surface of the methodologies used and the results obtained so
please do get in touch if you'd like further information about my research.

<br />

<h3>A new method to detect balancing selection</h3>
 
The role that balancing selection plays in the maintenance of genetic variation remains unknown. In humans,the signature of balancing selection has been detected at various 
genomic localities, but the overall frequency ofbalancing selection has yet to be quantified. Recent studies have identified loci under long term balancing selection in primates
by identifying polymorphisms shared between two species. These studies have utilised the fact that two speciesare extremely unlikely to share a neutral polymorphism (i.e. they 
are sufficiently divergent that all polymorphism that waspresent in the ancestor of the two species will have gone to fixation in at least one of the species). This makes these 
tests weak because balancing selection must persist for a long time. <br />

Together with our collaborator Michiel Vos at the University of Exeter, we present a simple solution that 
allows one to use closely related species or populations. Neutral polymorphisms are used to inform us as to what to expect 
under neutrality by comparing the number of polymorphisms shared between two populations, at putatively functional sites with those at putatively neutral sites. 
Through simulations we have proven that our statistic has power to detect balancing selection, as can be seen in figure 1.

 <figure>
  <img src="https://vivaksoni.github.io/_pages/Z.png" alt="Z" style="width:100%">
  <figcaption>Fig.1 - Simulating our statistic under neutrality (blue), with deleterious mutations introduced (orange), and with neutral, deleterious variation, and balancing selection. tMRCA is measured in N generations, where N is the population size. A log(Z) value of greater than 0 indicates a greater proportion of shared non-synonymous polymorphisms than private non-synonymous polymorphism, which is our signal of balancing selection. Note that although balancing selection elevates log(Z), this is in the absence of complex demography</figcaption>
</figure> 

We have applied this statistic to human population genetic data taken from the 1000 genome project. We simulated under the Gravel et. al (PNAS, 2011) to generate our null model, and compared this to our observed data. Although we detect balancing selection at low frequencies within humans, the evidence is weak due to the confounding effects of human demographic history because population contraction (for instance via bottlenecks) depresses our statistic. Nature can be 
frustrating at times!

<br />

<h3>Does the age of a protein-coding gene constrain its evolution?</h3>

How adaptation proceeds in space and time has long been a focus of study for molecular geneticists. The visualisation of fitness as a multi-dimensional landscape was first conceived of by Sewall Wright (Proceedings of the Sixth International Congress on Genetics, 1932) and fitness (or adaptive) landscapes have become a cornerstone of the study of adaptation in population and quantitative genetics. If genes adapt towards local fitness optima over time, one can hypothesise that younger genes are further away from fitness optima and therefore might be evolving more rapidly towards optima than older genes (that are already closer to an optimum).

 <figure>
  <img src="https://vivaksoni.github.io/_pages/adaptiveLandscape.png" alt="adaptiveLandscape" style="width:100%">
  <figcaption>Fig.2 - An example of an adaptive landscape. The mean fitness of the population is determined by the frequencies of allele A and allele B within the population.</figcaption>
</figure>

In this project we have correlated the rate of adaptive evolution with various gene age, whilst accounting for potentially confounding factors, including function, recombination rate, solvent accessibility, and intrinsic protein disorder. Our collaborators Ana Filipa Moutinho and Julien Duthiel at the Max Planck Institute for Evolutionary Biology have found a significant correlation between gene age and rates of adaptive evolution in Drosophila melanogaster and Arabidopsis thaliana.

 <figure>
  <img src="https://vivaksoni.github.io/_pages/geneAges.PNG" alt="geneAges" style="width:100%">
  <figcaption>Fig.3 - Relationship between the rate of protein evolution (ω), non-adaptive non-synonymous substitutions (ωNA), and adaptive non-synonymous substitutions (ωA) and log (gene age). Error bars denote for the 95% confidence interval for each category, computed over 100 bootstrap replicates. We see a surprisingly high correlation between gene ages and rates of non-adaptive evolution. Though it doesn't look like it, the correlation between the rate of adaptive evolution and gene age is significant, with a τ value of -0.4, obtained using a Kendall's rank correltion.</figcaption>
</figure> 

Although the correlation between gene age and rates of adaptive evolution is significant, we find that this correlation disappears when we account for confounding factors. We are working on some theory to understand the extent to which these estimates of adaptive evolution in humans are confounded by the population contraction from the human-chimp ancestor to the present day.

<br />

<h3>Gene-level and site-level factors affecting the rate of adaptive evolution in humans</h3>

Going very much hand in hand with the gene ages project discussed above, we have looked at various gene level and site level factors affecting the rate of adaptive evolution in humans. Although this project spans many different factors, here I will briefly describe some of our work in estimating rates of adaptive evolution across GO categories. Following Enard et. al (eLife, 2016), we compared the rates of adaptive evolution betweeen virus-interacting proteins (VIPs) and non-VIPs. Enard et al. found that the vast majority of adaptive evolution in humans is due to VIPs, but as figure 4 shows, we find adaptive evolution occuring both in VIPs and non-VIPs.

 <figure>
  <img src="https://vivaksoni.github.io/_pages/vips.png" alt="VIPs" style="width:100%">
  <figcaption>Fig.4 - Comparison of α estimates between VIPs and non-VIPs for each GO category.</figcaption>
</figure> 

To resolve whether the variation we see in rates of adaptive evolution between GO categories is mostly along the VIP/non-VIP axis we can estimate the error variance across both axes (VIP/nonVIP and each GO category). For each VIP and non-VIP GO category we randomly assigned polymorphisms and substitutions to two groups. We estimated the rate of adaptive evolution for each of these four groups: VIP group 1; VIP group 2; non-VIP group 1; and non-VIP group 2 and estimated the error variance both with and without the interaction term. In both instances the error is much higher across the VIP/non-VIP axis than across GO categories. We can therefore conclude that the variation in adaptive evolution is mostly due to differences between GO categories.

<br />

<h3>Quantifying the variation in the effective population size across the human genome</h3>

This is a project that is still in its infancy, and so I will just outline its remit. To estimate the distribution of the effective population size, Ne, across the genome we have two sources of information, the number of de novo mutations (DNMs), and the number of single nucleotide polymorphisms (SNPs), both of which are estimated across genomic windows of specific length. The number of DNMs per window just depends upon the mutation rate whereas the number of SNPs per window depends upon the mutation rate, the effective population size (Ne) and the length of the genealogy. If there is free recombination then every site has a different genealogy and with enough sites, this source of variance can be ignored. However, if there is limited recombination then this source of variation can be large. 

In this project we are attempting to quantify this variation. We will model the distribution of rates by fitting a distribution to our DNM data. We will then fit a distribution to our SNP data and look to infer the parameters of the distribution of Ne with or without free recombination.

