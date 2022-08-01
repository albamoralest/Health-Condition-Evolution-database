# Health Condition Evolution KG
 A database of Health Condition Evolution - HES
 
 KA pipeline
 
 ![Knowledge acquisition pipeline](/assets/KApipeline.png?raw=true "KA pipeline")
 

#### HECON Ontology

 [HECON Ontology repository](https://github.com/albamoralest/HECON-Ontology)
    
 ##### [Knowledge Graph construction](https://github.com/albamoralest/HECON-Ontology/tree/main/Knowledge%20Graph)
    data -> RDF data in TTL format
    queries -> SPARQL Anything queries for building RDF data
    rawData -> database of Health Evolution Statements in CSV format

#### Details of the data


1. Corpus preparation: 
    |_ 01trainingdataset
    The training dataset and preparation process
    
2. Knowledge components extraction: 
    |_ 02MLAlgorithms/
    Jupyter notebooks implementing (training and test process)the different algorithms used to classify sentences according to the HES.
    It also contains the models used to infer the HES
    
    |_ 03predictions/
    Jupyter notebooks with the application of the machine learning approach and predictions on the entire corpus
    
3. Knowledge completion: 
    Jupyter notebooks with the implementation of the propagation rules
    For the extraction of SNOMED CT concepts we work with Snowstorm. 
    Snowstorm is a SNOMED CT terminology server built on top of Elasticsearch, with a focus on performance and enterprise scalability.
    We use Snowstrom and ECL to query SNOMED CT taxonomy and obtain the list of features and relationships of each concept. 
    
    [Snowstrom reporsity by SNOMED CT ](https://github.com/IHTSDO/snowstorm)
    
    
4. Human-in-the-loop
    [Tool repository](https://github.com/albamoralest/evaluation_KA)
    
