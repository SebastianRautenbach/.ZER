
![](https://github.com/SebastianRautenbach/.ZER/blob/60d14ed8ff5886720a5561a56e1891b2c526478d/.zer2.png)
A semi-YAML serializer for c++ projects 

# -setting up a class
    filedata::ZER save_object;


# -stating variables
	save_object["player"]["movement"].set_float("variable_name", { 90., 90, 90 });
	save_object["player"].set_string("name_id", { "BOB" });
	save_object["player"].set_int("ID", { 908334233 });

# -save and load files
	save_object.read_file_cntx("save.zer");
	save_object.save_file(save_object, "save.zer");
 
# -retrieving variables
	save_object["player"]["movement"].get_float("variable_name"); //this retrieves the whole array
	save_object["player"].get_string("name_id")[0];   //this returns the first index of the array even if there is one value stored
	save_object["player"].get_int("ID")[0];     //this returns the first index of the array even if there is one value stored
