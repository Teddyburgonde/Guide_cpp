# Utilisation de map 

Map est un conteneur qui s'alloue automatiquement.

Exemple : 

```cpp
#include <iostream> 
#include <map> // Include nécessaire pour utiliser map

int	main()
{
	// Declaration d'un conteneur map
	std::map<std::string, double> students;
	
	// Initialisation de map 
	students["Pierre"] = 20.0;
	students["Jean"] = 10.0;
	students["Alice"] = 14.0; // Alice est en premiere position dans la map
	
	// map n'est pas indexées donc ne pas faire cela❗
	/* 
	for (int i = 0; i < students.size(); i++)
	{
		std::cout << students << std::endl;
	}
	*/

	/* Utilisation d'un iterator pour imprimer les valeurs de map */
	
	// Creation d'un type iterator qui peut parcourir un map de ce type.
	std::map<std::string, double>::iterator it; 
	
	// Iterator pointe vers le premier élément de la map.
	for(it = students.begin(); it != students.end(); ++it)
	{
		// Accède à la clé avec it->first  
		// Accède à la valeur associée à la clé it->second 
		std::cout << it->first << " a eu " << it->second << std::endl;
	}
	// La taille de map
	std::cout << "Le nombre de students dans le conteneur : " << students.size() << std::endl;
}
```

