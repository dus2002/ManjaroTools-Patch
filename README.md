# ManjaroTools-Patch
Parche para Manjaro Tools.
Éste parche permite añadir soporte para las ramas de 32 bits de Manjaro, para evitar errores al crear instaladores de 32 bits.

Cómo se hace FÁCIL:
Se sobreescribe sobre '/' éste repositorio.

Cómo se hace DIFÍCIL:
Se realizan las siguientes modificaciones:
 is_valid_branch(){
     case $1 in
         'stable'|'testing'|'unstable') return 0 ;;
+        'x32-stable'|'x32-testing'|'x32-unstable') return 0 ;;
         *) return 1 ;;
     esac
 }
