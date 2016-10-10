##Tarea: Recycler View
##Ana Gabriela García Páramo
___
RecyclerView es un contenedor de una cierta cantidad de elementos en forma de lista muy parecido a la clase ListView, nos permite volver a utilizar los items que ya no son visibles para el usuario debido al scrolling. También nos permite configurar una cierta cantidad de animaciones para ser desplazadas, eliminadas y crear nuevos elementos en tiempo real. 

Con la ayuda de la libreria de soporte v7Support Library se puede usar RecyclerView en dispositivos que ejecutan versiones anteriores de Android, agregando la siguiente linea en la sección de dependencias en el archivo build.gradle:

    compile 'com.android.support:recyclerview-v7:21.0.+'

Usando una instancia de ReciclerView podemos definirlo en un archivo XML Layout: 
    
    <android.support.v7.widget.RecyclerView
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:id="@+id/reciclador"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:padding="3dp"
        android:scrollbars="vertical" />

Un RecyclerView necesita un LayoutManager para manejar la posición de sus elementos, existen subclases LayoutManager predefinidas:  

* LinearLayoutManager
* GridLayoutManager
* StaggeredGridLayoutManager

Se deben tener los datos que sirvan como alimento para el adaptador. Para crear un adaptador que pueda ser usado en un RecyclerView se debe externder a RecyclerView.Adapter y define una clase interna que extiende a RecyclerView.ViewHolder. Un ViewHolder es un objeto que representa un ítem de la lista, el cual almacena las referencias de los views dentro del layout con propósitos de acceso rápido. 

