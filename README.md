# file-communicate
Registratie formulier is aangepast nu slaat hij alles wat je hebt ingevuld op in een yaml file. 
Dit zijn de codes die ik heb toegevoegd/aangepast
```python
mapName = "C:/Users/Gebruiker/Documents/ICT/file-communicate/databron"
if os.path.exists(mapName) != True:
    os.mkdir(mapName)

dataTitle = "data_(" + nameCheck + ")_" + str(datetime.datetime.now().timestamp()) + ".yaml"
fileName = "C:/Users/Gebruiker/Documents/ICT/file-communicate/databron/" + dataTitle
jsonForm = json.dumps(dictForm, indent=1)
with open (fileName, "x") as f:
    f.writelines(jsonForm)
```