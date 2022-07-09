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
{"id": 26760, "data": "There are so many cars on the highway that I cannot recognize but I think there is a yellow Jeep Renegade driving Right with 75 km/h and a rose-bloom Ford Taurus driving left at a speed of 53 kilometers per hour .", "ner_label": [["vehicle_color", 85, 91, "yellow", 18, 19, ["yellow"]], ["vehicle_brand", 92, 96, "Jeep", 19, 20, ["Jeep"]], ["vehicle_model", 97, 105, "Renegade", 20, 21, ["Renegade"]], ["vehicle_orientation", 114, 119, "Right", 22, 23, ["Right"]], ["vehicle_velocity", 125, 127, "75", 24, 25, ["75"]], ["vehicle_color", 139, 149, "rose-bloom", 28, 29, ["rose-bloom"]], ["vehicle_brand", 150, 154, "Ford", 29, 30, ["Ford"]], ["vehicle_model", 155, 161, "Taurus", 30, 31, ["Taurus"]], ["vehicle_orientation", 170, 174, "left", 32, 33, ["left"]], ["vehicle_velocity", 189, 211, "53 kilometers per hour", 37, 41, ["53", "kilometers", "per", "hour"]]], "re_label": [[0, 1, 2, 3, 4], [5, 6, 7, 8, 9]]}
{"id": 26761, "data": "There are so many cars on the highway that I cannot recognize but I think there is a yellow Jeep Renegade driving Right with 75 km/h and a rose-bloom Ford Taurus driving left at a speed of 53 kilometers per hour .", "ner_label": [["vehicle_type-suv", 92, 105, "Jeep Renegade", 19, 21, ["Jeep", "Renegade"]], ["vehicle_type-sedan", 150, 161, "Ford Taurus", 29, 31, ["Ford", "Taurus"]]]}
