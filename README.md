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
| Goal | Given customer utterances with subjective preference, to determine candidate attribute values. |
| Input | Current user utterance, Dialog History, Multimodal context |
| Output |  Candidate attribute values |
| Metrics | Disam F1 / Precision / Recall |

| Sub-Task #2 | Referred Region Understanding |
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| Goal | Given dialog history with region referring, to determine candidate object IDs. |
| Input | Dialog context, Multimodal context |
| Output |  Canonical object IDs |
| Metrics |  Refer F1 / Precision / Recall |

| Sub-Task #3-1 | Multimodal Recommendation - Act Prediction |
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| Goal | To track user belief states across multiple turns |
| Input | Current user utterance, Dialogue context, Multimodal context |
| Output | Belief state for current user utterance |
| Metrics | Slot F1, Intent F1 |

| Sub-Task #3-2 | Multimodal Recommendation - Response Generation |
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| Goal | To track user belief states across multiple turns |
| Input | Current user utterance, Dialogue context, Multimodal context |
| Output | Belief state for current user utterance |
| Metrics | Slot F1, Intent F1 |

| Sub-Task #3-3 | Multimodal Recommendation - Item Recommendation |
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| Goal | To track user belief states across multiple turns |
| Input | Current user utterance, Dialogue context, Multimodal context |
| Output | Belief state for current user utterance |
| Metrics | Slot F1, Intent F1 |
