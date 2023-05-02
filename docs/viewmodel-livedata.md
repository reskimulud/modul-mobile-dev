# ViewModel dan LiveData

## ViewModel

ViewModel adalah sebuah class yang dirancang untuk menyimpan dan mengelola data terkait UI dalam sebuah lifecycle yang tetap. ViewModel akan tetap hidup selama activity atau fragment yang terkait dengannya masih ada. Hal ini memungkinkan data yang disimpan di dalamnya tetap ada meskipun terjadi perubahan konfigurasi seperti rotasi layar.

## LiveData

LiveData adalah sebuah class yang dirancang untuk menyimpan dan mengelola data yang dapat diamati (observable) dari sebuah lifecycle. LiveData akan mengupdate UI ketika terjadi perubahan data. LiveData juga akan mengupdate UI ketika terjadi perubahan lifecycle.

**[<< Sebelumnya](aac.md)**  | [Selanjutnya >>](viewmodel-livedata-exercise.md)
