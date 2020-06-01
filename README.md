import xml
import json
import yaml

with open ('sample.json','r') as json_file:
    json_file_data = json.load(json_file)

with open ('sample.xml','t') as xml_file:
    xml_file.write(xmltodict.unparse(json_file_data))
    
with open ('sample.yaml','w') as yaml_data:
    yaml_file = yaml.dump(json_file_data , yaml_data)
    
