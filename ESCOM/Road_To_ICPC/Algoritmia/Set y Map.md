### Map
Puede verse como un diccionario en python. Le puedes pasar algun dato, del tipo que sea y te dará como resultado algo, y a esto se le llama tabla de hasheo o hash map
Podemos tener algo como los siguiente
map<string,int> mapa;
"HOLA"->1
"ADIOS"->1
"HOLA"->2 ----- Esto no se puede ya que hay dos HOLA, necesitamos escoger uno solo

#### Operaciones
mapa.empty(); ver si está vacío
mapa["HOLA"]=3
mapa.contains(HOLA); //Regresa TRUE O FALSE. Solo c++ 23
mapa.erase("HOLA"); //Eliminar el elemento
mapa.size();
**los mapas se pueden ver como un espacio de memoria**