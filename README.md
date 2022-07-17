# Generating supervised machine learning pipelines using genetic programming

As part of my Master's Thesis, I developed a way to generate supervised machine learning pipelines using genetic programming to solve multinomial classification problems. Following libraries and research papers were my inspiration to try applying this technique:
- http://epistasislab.github.io/tpot/
    - [[OBUM16]](https://dl.acm.org/doi/10.1145/2908812.2908918) Randal S. Olson, Nathan Bartley, Ryan J. Urbanowicz, Jason H. Moore. Evaluation of
a tree-based pipeline optimization tool for automating data science. Proceedings of the
Genetic and Evolutionary Computation Conference 2016, GECCO ’16, pages 485–492,
New York, NY, USA, 2016. ACM.
- https://laic-ufmg.github.io/Recipe/docs/about/
    - [[dSPOP17]](https://link.springer.com/chapter/10.1007/978-3-319-55696-3_16) Alex Guimarães Cardoso de Sá, Walter José G. S. Pinto, Luiz Otávio Vilas Boas Olive-
ira, Gisele L. Pappa. RECIPE: A grammar-based framework for automatically evolving
classification pipelines. EuroGP, Lecture Notes in Computer Science, vol 10196. Springer,
pages 246–261, 2017.

### What was my idea about?:

In order to represent supervised machine learning pipelines, my idea was to come up with a representation of attribute trees and their repositories of hyperparameters as words of a language defined programmable attribute graph grammar [[Bun82]](https://ieeexplore.ieee.org/document/4767310), [[Bun83]](https://link.springer.com/chapter/10.1007/BFb0000096).

With this approach, I was able to use genetic programming [[Cra85]](https://dl.acm.org/doi/10.5555/645511.657085), [[Koz92]](https://link.springer.com/article/10.1007/BF00175355) to generate machine learning pipelines and look for the best one.

Excerpt from my Master's Thesis is available [here](/Generating_supervised_machine_leraning_pipelines_using_genetic_programming_excerpt_in_Polish.pdf). I share everything needed to implement the idea. Starting with a defined grammar, embedding transformations, a control diagram and custom genetic programming operators. Shared excerpt is available in Polish.

### Some examples:

Example use of production of my defined grammar:

![Example use of production of defined grammar](/img/4.png)

Example of my crossover operation:

![Example of my crossover operation](/img/1.png)

Example of my mutation operation:

![Example of my mutation operation](/img/2.png)

A prototype showing how my idea works has been implemented in Scala using Apache Spark.

![Example of prototype outcome](/img/3.png)

I do not share the implementation due to the fact that the entire solution was a prototype. Usually, prototypes don't go hand-in-hand with good code quality.

## References:

### Reaserch papers: 

- [[Bun82]](https://ieeexplore.ieee.org/document/4767310) Horst Bunke. Attributed programmed graph grammars and their application to schematic
diagram interpretation. IEEE Transactions on Pattern Analysis and Machine Intelligence,
PAMI-4(6):574–582, Nov 1982.
- [[Bun83]](https://link.springer.com/chapter/10.1007/BFb0000096) Horst Bunke. Graph grammars as a generative tool in image understanding. Hartmut
Ehrig, Manfred Nagl, Grzegorz Rozenberg, redaktorzy, Graph-Grammars and Their Ap-
plication to Computer Science, pages 8–19, Berlin, Heidelberg, 1983. Springer Berlin
Heidelberg.
- [[Cra85]](https://dl.acm.org/doi/10.5555/645511.657085) Nichael L. Cramer. A representation for the adaptive generation of simple sequential
programs. Proceedings of the 1st International Conference on Genetic Algorithms, pages
183–187, Hillsdale, NJ, USA, 1985. L. Erlbaum Associates Inc.
- [[Koz92]](https://link.springer.com/article/10.1007/BF00175355) John R. Koza. Genetic Programming: On the Programming of Computers by Means of
Natural Selection. MIT Press, Cambridge, MA, USA, 1992.

### Links:
- http://epistasislab.github.io/tpot/,
- https://laic-ufmg.github.io/Recipe/docs/about/,
- https://automl.github.io/auto-sklearn/master/,
- https://www.cs.ubc.ca/labs/algorithms/Projects/autoweka/.

### More links to mainstream AutoML (automated machine learning) solutions:
- https://azure.microsoft.com/en-us/services/machine-learning/automatedml/,
- https://aws.amazon.com/machine-learning/automl/,
- https://cloud.google.com/automl/,
- https://docs.databricks.com/applications/machine-learning/automl.html,
- https://www.datarobot.com/platform/automated-machine-learning/,
- https://rapidminer.com/platform/automated-data-science/.
