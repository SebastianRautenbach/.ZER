# .ZER
Serializer for c++ projects 

# -setting up a class
    filedata::ZER save_object;


# -stating variables
	save_object["player"]["movement"].set_float("variable_name", { 90., 90, 90 });
	save_object["player"].set_string("name_id", { "BOB" });
	save_object["player"].set_int("ID", { 908334233 });

# -save and load files
	save_object.read_file_cntx("save.zer");
	save_object.save_file(save_object, "save.zer");
