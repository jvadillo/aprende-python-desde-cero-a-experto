# Tuplas
Las tuplas son **listas inmutables**. Es decir, una vez declaradas, no se pueden realizar modificaciones sobre ellas (añadir/eliminar elementos o hacer modificaciones sobre ellos). Para definir una tupla se escriben los elementos entre paréntesis:

    valores = (1,2,3)

El acceso a sus elementos se hace de igual que con listas:

    valores = ("a", "b", "c","d","e","f")  
    print(valores[1])
    print(valores[2:4])

Una acción típica de las tuplas es "desempaquetar" (unpack) sus valores:

    a, b, c = valores 
