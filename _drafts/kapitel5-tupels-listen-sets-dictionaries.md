# Listen
numList = [1, 2, 3]
featureList = ["Strassen", "Wege", "Postleitzahlen"]
feat = featureList[1]
featureList[1] = "Garten"
feat2 = featureList[0:2]
len() geht
Listen können mit + zusammengefügt werden
append()
sort()
featureList[1:3] = ["Garten","Haus"]

Lists sind veränderbare Datentypen und deswegen beziehen sich Veränderungen auf alle Referenzen (Pass by Reference)


# Dictionaries
dicTel = {"Austria" : "0043", "Germany" : "0049", "Switzerland" : "0041"}
print dicTel["Germany"]
dicTel["Germany"] = "+49"

len()
del dicTel["Germany"]      (löscht das Paar)
"0043" in dicTel      schaut ob Schlüssel da ist
keys()
values()
clear()ngen auf alle Referenzen (Pass by Reference)