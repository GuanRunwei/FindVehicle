# ***FindVehicle***
***FindVehicle***: A NER dataset in transportation to extract keywords describing vehicles on the road

## Dataset Download
Data Link: [Baidu Cloud Disk](https://pan.baidu.com/s/1NIuDeeIba-eKU5WtIY44nQ)

Password: tbr6

## Dataset Directory
***FindVehicle*** has 2 data formats, CoNLL-style and jsonlines. 
### CoNLL-style format
  - FindVehicle_train.txt -> Train set, CoNLL-style Annotation, NER Label
  - FindVehicle_test.txt -> Test set, CoNLL-style Annotation, NER Label

*CoNLL-style Example (Flat Entity)*
> I O  <br>
> am O <br>
> looking O  <br>
> for O  <br>
> a O  <br>
> white B-vehicle_color  <br>
> sedan B-vehicle_type  <br>
> . O  <br>

*CoNLL-style Example (Overlapped Entity)*
> I O  <br>
> am O  <br>
> looking O  <br>
> for O  <br>
> a O  <br>
> white B-vehicle_color  <br>
> Audi B-vehicle_brand  <br>
> Q7 B-vehicle_model  <br>
> . O  <br>
> 
>
> I O  <br>
> am O  <br>
> looking O  <br>
> for O  <br>
> a O  <br>
> white B-vehicle_color  <br>
> Audi B-vehicle_type-suv  <br>
> Q7 E-vehicle_type-suv  <br>
> . O  <br>


### jsonlines format
  - FindVehicle_train.jsonl -> Train set, jsonlines format, NER Label, RE Label
  - FindVehicle_test.jsonl -> Test set, jsonlines format, NER Label, RE Label
  
![test](https://github.com/GuanRunwei/FindVehicle/blob/main/images/ner_annotation_format.png)

*jsonlines Example*
"ner_label":[
              [
                 label, char span start index, char span end index, char span check, token span start index, token span end index, token span check
              ]
            ]
