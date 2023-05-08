# Experiments

## Analysis of Prior Work

In this experiment, 16 studies from 7 different work: Rose & Nichols (2019, 2020); Gelman & Wellman (1991); Keil(1992); Waxman et al. (2007); Hampton et al.(2007); Barton & Komatsu(1989) were chosen for replication on language models because they are representative of research that has used <b>transformation tasks</b> and <b>nature vs. nurture tasks</b> to investigate essentialist categorization across various domains. GPT-3 (Model: text-curie-001) and BLOOM were given the materials and returned open ended responses. The language models were asked to respond to each question in the materials 50 times.  The materials that we used to query the language models can be found in `aopw_tasks_collection_essentialism.csv`. 

The examples that were given to GPT-3 for training it to complete the answer retrival task can be found in `aopw_response_trainer.csv` or `aopw_response_trainer.txt`. To directly use it, simply copy the content in `aopw_response_trainer.txt` without the divison lines inside 

```python
prefix_prompt = """


"""
```
 and run the script called `aopw_gpt3_answer_retrieval_cached.ipynb` for GPT-3 and `aopw_bloom_answer_retrieval_cached.ipynb` for BLOOM in `/python`.

## Experiment 1

In this experiment, GPT-3 (Model: text-davinci-002) and BLOOM were given vignettes that involved a thing undergoing a special procedure so that it either had the same or different appearance and had either the original thing’s telos or a different telos. After the vignette, the language models were asked to categorize if the thing after the special operation an original or a new thing. 

>**_NOTE:_** The items employed in this experiment were also used in Experiment 2 and 3.

The language models were requested to complete categorization tasks for three domains - Living Natural Kind, Non-living Natural Kind, and Artifact. Each domain had four items, resulting in 12 possible item pairs. To control for potential order effects, the order of telos and appearance information shown in the prompt was counterbalanced. Each language model was tasked to respond to each pair of items five times. 

Altogether, the language models made <i>1440</i> judgments during this experiment. 

> **_NOTE:_** Appearance(original, new) * Telos(preserved, changed) * Appearance | Telos sentence order * Queried 5 times * 12 Item pairs per domain * 3 Domains


The materials that we used to query the language models can be found in `experiment1_tasks_collection_essentialism.csv`.


## Experiment 2

This experiment had the same design as experiment 3. The difference was that instead of presenting telos information in the vignettes, "made of " information was presented to the language models.

Altogether, the language models made <i>1440</i> judgments during this experiment. 

> **_NOTE:_** Appearance(original, new) * Made of(preserved, changed) * Appearance | Made of sentence order * Queried 5 times * 12 Item pairs per domain * 3 Domains


The materials that we used to query the language models can be found in `experiment2_tasks_collection_essentialism.csv`.


## Experiment 3

The design of this experiment closely resembled that of Experiment 2 and 3. The only difference was that the vignettes were expanded to incorporate both telos and "made of" information. The variations tested whether objects underwent changes in appearance, composition, or purpose across transformations -- whether a thing had preserved or changed appearance, preserved or changed what it is made of, and preserved or changed its telos across transformations.

Altogether, the language models made <i>2880</i> judgments during this experiment. 

> **_NOTE:_** Appearance(original, new) * Telos(preserved, changed) * Made of(preserved, changed) * Telos | Made of sentence order * Queried 5 times * 12 Item pairs per domain * 3 Domains

> **_NOTE:_** Appearance wasn't counterbalanced in this experiment since it didn't seem to matter in Experiment 1 and 2.


The materials that we used to query the language models can be found in `experiment3_tasks_collection_essentialism.csv`.
