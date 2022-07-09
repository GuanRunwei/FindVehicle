# ***FindVehicle***
***FindVehicle***: A NER dataset in transportation to extract keywords describing vehicles on the road

![test](https://github.com/GuanRunwei/FindVehicle/blob/main/images/ner_types.png =100x100)

## Dataset Download
Data Link: [Baidu Cloud Disk](https://pan.baidu.com/s/1NIuDeeIba-eKU5WtIY44nQ)

Password: tbr6

## Dataset Directory
***FindVehicle*** has 2 data formats, CoNLL-style and jsonlines. 
### CoNLL-style format
  - FindVehicle_train.txt -> Train set, CoNLL-style annotation, NER Label
  - FindVehicle_test.txt -> Test set, CoNLL-style annotation, NER Label

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
  - FindVehicle_train.jsonl -> Train set, jsonlines annotation, NER Label, RE Label
  - FindVehicle_test.jsonl -> Test set, jsonlines annotation, NER Label, RE Label

*jsonlines Example*

> { <br>
>     "id": 41628,  <br>
>     "data": "Let the clever boy help find out the Silver XPeng G3 and lemon yellow Chevrolet Trailblazer in the Bottom Left of the image that driven left .",   <br>
>     "ner_label": [  <br>
>     ["vehicle_color", 37, 43, "Silver", 8, 9, ["Silver"]],  ### label, char span start index, char span end index, char span check, token span start index, token > > span end index, token span check <br>
>     ["vehicle_brand", 44, 49, "XPeng", 9, 10, ["XPeng"]],   <br>
>     ["vehicle_model", 50, 52, "G3", 10, 11, ["G3"]],   <br>
>     ["vehicle_color", 57, 69, "lemon yellow", 12, 14, ["lemon", "yellow"]],   <br>
>     ["vehicle_brand", 70, 79, "Chevrolet", 14, 15, ["Chevrolet"]],   <br>
>     ["vehicle_model", 80, 91, "Trailblazer", 15, 16, ["Trailblazer"]],   <br>
>     ["vehicle_location", 99, 110, "Bottom Left", 18, 20, ["Bottom", "Left"]],   <br>
>     ["vehicle_orientation", 99, 105, "Bottom", 18, 19, ["Bottom"]]],   <br>
>     "re_label": [[0, 1, 2, 6, 7], [3, 4, 5, 6, 7]]  <br> ### the indexes 0,1,2,6,7 refer to one target, indexes 3,4,5,6,7 refer to one target.
> }
