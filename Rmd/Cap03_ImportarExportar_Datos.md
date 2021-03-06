<style>
.small-code pre code {
  font-size: 1em;
}
</style>


PROGRAMACIÓN Y DATA SCIENCE CON R
========================================================
author: Nestor Montaño
date: Octubre.2017
autosize: true
transition: rotate
<small> 
Vicerrectorado de Formación Académica y Profesional    
Universidad de Guayaquil
</small>



Importación y Exportación de Datos - Bases
========================================================
type: sub-section



Importar csv
========================================================

- Desde RStudio  
  Import Dataset > From Text File > Escoger archivo > Abrir > Escribir nombre a la variable > Import
- Con comando    
  read.csv( file, sep = "," , dec = "," , stringsAsFactors= FALSE)
- Para grandes volúmenes de datos usar paquete data.table   
  fread()



Importar desde excel
========================================================

- Copiando desde un archivo de excel abierto  
  read.table("clipboard", sep="\t", header=TRUE)
- Desde RStudio  
  Rstudio > Import Dataset > From Excel > Escoger archivo > Abrir > Escribir nombre a la variable > Import
- Usando el paquete `openxlsx`  
  read.xlsx(xlsxFile , sheet , startRow , colNames , skipEmptyRows, rowNames)  
  data_tiempo_espera <- read.xlsx(xlsxFile = 'Data/Data_Banco.xlsx')  
- Otros paquetes  
  `excel.link`, `XLConnect`, `xlsx`, `readxl`, `rio`


Importar desde excel - Openxlsx
========================================================

- Descargar [Rtools] (https://cran.r-project.org/bin/windows/Rtools/)
- Instalar Rtools
  - Se debe escoger "agregar al path"
  - Si la computadora ya tiene CYGWIN, se tiene un tratamiento especial
- Instalar el paquete `openxlsx`  
- Activar el paquete `openxlsx`  
- Para leer se usa el comando read.xlsx(xlsxFile , sheet , startRow , colNames , skipEmptyRows, rowNames)  
  - Considerar que luego de importado el archivo se debe verificar los tipos de datos
  
  

Exportar a excel
========================================================

- Usando el paquete `openxlsx`  
  write.xlsx(x, file, asTable = FALSE, ...)
- Se puede usar los paquetes `XLConnect`, `xlsx`, etc.
  



Importar desde SPSS, SAS, Stata, etc
========================================================

- Desde RStudio  
  Rstudio > Import Dataset > From SPSS/SAS/STATA
- Usando el paquete `foreign`  
  SAS: read.xport()  
  SPSS: read.spss()  
  Stata: read.dta()  
  Soporta otros formatos
- Usango el paquete `haven`  
  SAS: read_sas() y read_xpt()   
  SPSS: read_sav() y read_por()  
  Stata: read_dta()   
- Se puede usar el paquerte `rio`  
  


Exportar a SPSS, SAS, Stata, etc
========================================================

- Usango el paquete `foreign`    
  write.foreign(df, datafile, codefile, package = c("SPSS", "Stata", "SAS"), ...)
- Usango el paquete `haven`  
  SAS: write_sas()  
  SPSS: write_sav()  
  Stata: write_dta()  
- Se puede usar el paquerte `rio`



Interacción con Bases de Datos
========================================================

- Utilizando ODBC `RODBC`   
  (Recomendado para Microsoft SQL)
- Utilizando JDBC `RJDBC`   
  (Usa java DBC)
- Paquetes para bases específicas  
  RMySQL, ROracle, RPostgreSQL, RSQLite, mongolite, RMongo, MonetDB.R, rmongodb


 
Otros
========================================================

- GIS sistemas de información geográfica con `rgal` y `raster`
- GoogleSpreadSheets con `googlesheets`
- Archivos Open Document Spreadsheets con `readODS`
- JSON data con `rjson` o `jsonlite` o `RJSONIO`



Otros
========================================================


