## README WIP

How to use what's in here?

1. Clone this repository.
2. Download [RMLmapper](https://github.com/RMLio/rmlmapper-java) and [jarrrml-parser](https://github.com/RMLio/yarrrml-parser).
3. If you don't have it yet, download necessary data, for example using [get_data.ipynb](https://github.com/kasprzakj/radon_kg_mapping/tree/main/data_acquisition/get_data.ipynb) into `data/{dataset_name}.json` as per the current example in `get_data.ipynb`.
4. If you've made changes/created a new yarrrml file, it should be placed in this folder.
5. Open command line in the root project folder.
6. Run `yarrrml-parser -i yarrrml_files/yaml_file_name.yml -o mappings/mapping_file_name.rml.ttl`.
7. Run `java -jar rmlmapper.jar -m mappings/mapping_file_name.rml.ttl -o turtles/graph_file_name.ttl -s turtle`.
8. You should now have a .ttl file in `turtles`.

An example for 6 and 7:

`yarrrml-parser -i yarrrml_files/branches.yml -o mappings/branches.rml.ttl`

`java -jar rmlmapper.jar -m mappings/branches.rml.ttl -o turtles/branches.ttl -s turtle`