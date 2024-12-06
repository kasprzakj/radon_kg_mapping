## README WIP

How to use what's in here?

1. Download RMLMAPPER and jarrrml-parser (look it up, rmlmapper is a .jar file and the parser is to be installed in cmd and is somehow related to node.js I think)
2. Set up a venv using requirements.txt (optional)
3. Download the data using `get_data.ipynb` into `data/{dataset_name}.json` as per the current example in `get_data.ipynb`
4. If you've made changes/created a new yarrrml file, it should be placed in `yarrrml_files`
5. Open CMD in the root project folder
6. Run `yarrrml-parser -i yarrrml_files/{dataset_name}.yml -o mappings/{dataset_name}.rml.ttl`
7. Run `java -jar rmlmapper.jar -m mappings/{dataset_name}.rml.ttl -o turtles/{dataset_name}.ttl -s turtle`
8. You should now have a .ttl file in `turtles`

Example for 7 and 8:

`yarrrml-parser -i yarrrml_files/branches.yml -o mappings/branches.rml.ttl`

`java -jar rmlmapper.jar -m mappings/branches.rml.ttl -o turtles/branches.ttl -s turtle`

Note: currently existing `branches_single.yaml` specifies a different file (see: sources), I used it for testing, just a single branch in data/example/branch.json. This file **won't** work for the `data/branches.json` obtained using `get_data.ipynb`.