# Tokenization Examples

## Stage 2: Baseline Tokenization

### gpt2

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['n', 'eph', 'rol', 'ith', 'iasis'] | 5 |
| gastroesophageal | ['g', 'ast', 'ro', 'es', 'oph', 'age', 'al'] | 7 |
| dermographism | ['der', 'm', 'ograph', 'ism'] | 4 |
| electrocardiogram | ['elect', 'ro', 'card', 'i', 'ogram'] | 5 |
| immunohistochemistry | ['im', 'mun', 'oh', 'ist', 'ochemistry'] | 5 |
| acetylcholinesterase | ['acet', 'yl', 'ch', 'ol', 'ines', 'ter', 'ase'] | 7 |
| hypercholesterolemia | ['hyper', 'ch', 'olester', 'ole', 'mia'] | 5 |
| hepatocellular | ['he', 'p', 'ato', 'cell', 'ular'] | 5 |
| neurodegenerative | ['ne', 'uro', 'deg', 'ener', 'ative'] | 5 |
| myocardial | ['my', 'ocard', 'ial'] | 3 |

### bert_base

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['ne', '##ph', '##rol', '##ith', '##ias', '##is'] | 6 |
| gastroesophageal | ['gas', '##tro', '##es', '##op', '##ha', '##ge', '##al'] | 7 |
| dermographism | ['der', '##mo', '##graph', '##ism'] | 4 |
| electrocardiogram | ['electro', '##card', '##io', '##gram'] | 4 |
| immunohistochemistry | ['im', '##mun', '##oh', '##isto', '##chemist', '##ry'] | 6 |
| acetylcholinesterase | ['ace', '##ty', '##lch', '##olin', '##ester', '##ase'] | 6 |
| hypercholesterolemia | ['hyper', '##cho', '##les', '##terol', '##emia'] | 5 |
| hepatocellular | ['he', '##pa', '##to', '##cellular'] | 4 |
| neurodegenerative | ['ne', '##uro', '##de', '##gen', '##erative'] | 5 |
| myocardial | ['my', '##oca', '##rdial'] | 3 |

### biobert

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['ne', '##ph', '##rol', '##ith', '##ias', '##is'] | 6 |
| gastroesophageal | ['gas', '##tro', '##es', '##op', '##hage', '##al'] | 6 |
| dermographism | ['der', '##mo', '##graph', '##ism'] | 4 |
| electrocardiogram | ['electro', '##card', '##io', '##gram'] | 4 |
| immunohistochemistry | ['im', '##mu', '##no', '##his', '##to', '##chemistry'] | 6 |
| acetylcholinesterase | ['ace', '##ty', '##l', '##cho', '##lines', '##tera', '##se'] | 7 |
| hypercholesterolemia | ['h', '##yper', '##cho', '##les', '##tero', '##lem', '##ia'] | 7 |
| hepatocellular | ['he', '##pa', '##to', '##cellular'] | 4 |
| neurodegenerative | ['ne', '##uro', '##de', '##gene', '##rative'] | 5 |
| myocardial | ['my', '##oc', '##ard', '##ial'] | 4 |


## Stage 4: Baseline vs Custom Tokenization

### biomedical_bpe_100k

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['nephrolithiasis'] | 1 |
| gastroesophageal | ['gastroesophageal'] | 1 |
| dermographism | ['dermo', 'graph', 'ism'] | 3 |
| electrocardiogram | ['electrocardiogram'] | 1 |
| immunohistochemistry | ['immunohistochemistry'] | 1 |
| acetylcholinesterase | ['acetylcholinesterase'] | 1 |
| hypercholesterolemia | ['hypercholesterolemia'] | 1 |
| hepatocellular | ['hepatocellular'] | 1 |
| neurodegenerative | ['neurodegenerative'] | 1 |
| myocardial | ['myocardial'] | 1 |

### biomedical_bpe_50k

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['nephrolithiasis'] | 1 |
| gastroesophageal | ['gastroesophageal'] | 1 |
| dermographism | ['dermo', 'graph', 'ism'] | 3 |
| electrocardiogram | ['electrocardiogram'] | 1 |
| immunohistochemistry | ['immunohistochemistry'] | 1 |
| acetylcholinesterase | ['acetylcholinesterase'] | 1 |
| hypercholesterolemia | ['hypercholesterolemia'] | 1 |
| hepatocellular | ['hepatocellular'] | 1 |
| neurodegenerative | ['neurodegenerative'] | 1 |
| myocardial | ['myocardial'] | 1 |

### biomedical_bpe_30k

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['nephrolithiasis'] | 1 |
| gastroesophageal | ['gastroesophageal'] | 1 |
| dermographism | ['dermo', 'graph', 'ism'] | 3 |
| electrocardiogram | ['electrocardiogram'] | 1 |
| immunohistochemistry | ['immunohistochemistry'] | 1 |
| acetylcholinesterase | ['acetyl', 'cholinesterase'] | 2 |
| hypercholesterolemia | ['hypercholesterolemia'] | 1 |
| hepatocellular | ['hepatocellular'] | 1 |
| neurodegenerative | ['neurodegenerative'] | 1 |
| myocardial | ['myocardial'] | 1 |

### gpt2

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['n', 'eph', 'rol', 'ith', 'iasis'] | 5 |
| gastroesophageal | ['g', 'ast', 'ro', 'es', 'oph', 'age', 'al'] | 7 |
| dermographism | ['der', 'm', 'ograph', 'ism'] | 4 |
| electrocardiogram | ['elect', 'ro', 'card', 'i', 'ogram'] | 5 |
| immunohistochemistry | ['im', 'mun', 'oh', 'ist', 'ochemistry'] | 5 |
| acetylcholinesterase | ['acet', 'yl', 'ch', 'ol', 'ines', 'ter', 'ase'] | 7 |
| hypercholesterolemia | ['hyper', 'ch', 'olester', 'ole', 'mia'] | 5 |
| hepatocellular | ['he', 'p', 'ato', 'cell', 'ular'] | 5 |
| neurodegenerative | ['ne', 'uro', 'deg', 'ener', 'ative'] | 5 |
| myocardial | ['my', 'ocard', 'ial'] | 3 |

### bert_base

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['ne', '##ph', '##rol', '##ith', '##ias', '##is'] | 6 |
| gastroesophageal | ['gas', '##tro', '##es', '##op', '##ha', '##ge', '##al'] | 7 |
| dermographism | ['der', '##mo', '##graph', '##ism'] | 4 |
| electrocardiogram | ['electro', '##card', '##io', '##gram'] | 4 |
| immunohistochemistry | ['im', '##mun', '##oh', '##isto', '##chemist', '##ry'] | 6 |
| acetylcholinesterase | ['ace', '##ty', '##lch', '##olin', '##ester', '##ase'] | 6 |
| hypercholesterolemia | ['hyper', '##cho', '##les', '##terol', '##emia'] | 5 |
| hepatocellular | ['he', '##pa', '##to', '##cellular'] | 4 |
| neurodegenerative | ['ne', '##uro', '##de', '##gen', '##erative'] | 5 |
| myocardial | ['my', '##oca', '##rdial'] | 3 |

### biobert

| term | pieces | n_pieces |
|---|---|---:|
| nephrolithiasis | ['ne', '##ph', '##rol', '##ith', '##ias', '##is'] | 6 |
| gastroesophageal | ['gas', '##tro', '##es', '##op', '##hage', '##al'] | 6 |
| dermographism | ['der', '##mo', '##graph', '##ism'] | 4 |
| electrocardiogram | ['electro', '##card', '##io', '##gram'] | 4 |
| immunohistochemistry | ['im', '##mu', '##no', '##his', '##to', '##chemistry'] | 6 |
| acetylcholinesterase | ['ace', '##ty', '##l', '##cho', '##lines', '##tera', '##se'] | 7 |
| hypercholesterolemia | ['h', '##yper', '##cho', '##les', '##tero', '##lem', '##ia'] | 7 |
| hepatocellular | ['he', '##pa', '##to', '##cellular'] | 4 |
| neurodegenerative | ['ne', '##uro', '##de', '##gene', '##rative'] | 5 |
| myocardial | ['my', '##oc', '##ard', '##ial'] | 4 |

