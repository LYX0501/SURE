# Multimodal Recommendation Dialog with SUbjective PREference (SURE) 

We introduces a new dataset SURE (Multimodal Recommendation Dialog with SUbjective PREference), which contains 12K shopping dialogs in complex store scenes. The data is built in two phases with human annotations to ensure quality and diversity. SURE is well-annotated with subjective preferences and recommendation acts proposed by sales experts. A comprehensive analysis is given to reveal the distinguishing features of SURE. Three benchmark tasks are then proposed on the data to evaluate the capability of multimodal recommendation agents. Based on the SURE, we propose a baseline model, powered by a state-of-the-art multimodal model, for these tasks. 


<figure>
<img src="./overview-sure.png" width="550" alt="Illustration of the SURE Dataset" align="center"> 
<figcaption><i>Illustration of the SURE Dataset</i></figcaption> 
</figure>

## Track Description
### Tasks and Metrics
| Sub-Task #1 | Subjective Preference Disambiguation |
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| Goal | To determine candidate attribute values according subjective preference. |
| Input | Dialog history with subjective preference in the latest round, Multimodal context |
| Output | Candidate attribute values |
| Example | Customer: "I prefer color of happiness." <br> → yellow, brown, red |
| Metrics | Disam F1 / Precision / Recall |

| Sub-Task #2 | Referred Region Understanding |
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| Goal | To determine candidate object IDs according to regional reference. |
| Input | Dialog history with regional reference in the latest round, Multimodal context |
| Output |  Candidate object IDs |
| Example | Salesperson: "Look at the shelf on the right. Are there any clothes that you like?" <br> Customer: "Sorry, there is no garment that I am looking for in this region." <br> → 12, 13, 16, 22, 31 |
| Metrics |  Refer F1 / Precision / Recall |

| Sub-Task #3-1 | Multimodal Recommendation - Act Prediction |
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| Goal | To predict the salesperson's act in the next dialog round |
| Input | Dialog history, Multimodal context |
| Output | Act of salesperson in the next dialog round |
| Example | Salesperson: "The price $299 is too expensive for me to afford" <br> → Revise Attribute |
| Metrics | Act F1 |
| **Sub-Task #3-2** | **Multimodal Recommendation - Response Generation** |
| Goal | To generate the salesperson's utterance in the next dialog round |
| Input | Dialog history, Multimodal context |
| Output | Salesperson's utterance in the next dialog round |
| Example |  Customer: "I’d like to buy a sofa made by materials obtained from nature" <br> → Salesperson: "You can consider the leather material, which is natural and smooth." |
| Metrics | BLEU-4 / ROUGH-L / METEOR |
| **Sub-Task #3-3** | **Multimodal Recommendation - Item Recommendation** |
| Goal | To predict the target object in the last round of dialog |
| Input | Dialog history without last round, Multimodal context |
| Output | Target object ID |
| Example | (Dialog history) → Salesperson: "What are your thoughts on the black, unadorned overcoat? <@1032>" |
| Metrics | Recom F1 |

## Citation
If you want to publish experimental results with our datasets or use the baseline models, please cite the following articles:


## Lisence
SURE is released under [CC-BY-NC-SA-4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode), see [LICENSE](LICENSE) for details.
