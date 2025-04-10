Este ejercicio esta realizado, con Docker, donde se crea un contenedor preconfigurado con Hadoop el cual ya se encuentra instalado
se lanzar un clúster completo de Hadoop en minutos y simula un entorno distribuido sin necesidad de varias máquinas físicas.
Todos los contenedores se comunican en red interna (por ejemplo, usando docker-compose).
Cada contenedor actúa como un nodo virtual de Hadoop: Tiene Java y Hadoop instalados, su configuración (core-site.xml, hdfs-site.xml, etc.), este se conecta con los demás contenedores usando nombres de host definidos y se ejecutan servicios como namenode, datanode, resourcemanager, nodemanager.
Se sube y procesa un archivo .txt
Se procede a Entrar al contenedor del NameNode, usamos hdfs dfs -put para subir el archivo a HDFS, ejecutamos un job MapReduce como wordcount
y los DataNodes procesan partes del archivo en paralelo
El resultado se guarda en HDFS (y puedes leerlo con hdfs dfs -cat)
