# IMEIs-Lookup
Este script carga archivos Excel de pedidos y stock, normaliza columnas, mapea grados, filtra el stock según cantidad y condición de batería, y guarda los resultados en un nuevo archivo Excel. Maneja errores y notifica sobre pedidos no satisfechos.

Filtrado de Datos Completo 2
Este proyecto está diseñado para procesar y filtrar datos de dos archivos Excel: uno de pedidos y otro de stock. El objetivo es asignar el stock disponible a los pedidos según ciertos criterios y generar un archivo Excel con los resultados.

Funciones Principales
1. Carga de Archivos Excel

def load_excel_files(pedido_path, stock_path):

"""Carga los archivos Excel de pedido y stock en DataFrames de pandas."""

Carga los archivos Excel de pedidos y stock en DataFrames de pandas, manejando posibles errores de lectura.

2. Normalización de Columnas

def normalize_columns(df, column_name):

"""Convierte una columna a minúsculas y elimina espacios."""

Convierte una columna a minúsculas y elimina espacios para asegurar consistencia en los datos.

3. Mapeo de Grados

def map_grades(df, grade_column):
    """Mapea los valores de grado ('a', 'b', 'c') a ('mint', 'good', 'fair')."""
    
Mapea los valores de grado ('a', 'b', 'c') a ('mint', 'good', 'fair') y maneja valores no mapeados.

4. Filtrado por Cantidad y Condición de Batería

def filter_by_qty_and_battery(df_pedido, df_stock_original):
    """
    Filtra el DataFrame de stock basado en los requisitos del DataFrame de pedido,
    manejando cantidad y condición de batería, notifica sobre pedidos no satisfechos,
    y calcula el total de unidades faltantes.
    """

Filtra el stock basado en los requisitos del pedido, manejando cantidad y condición de batería, notificando sobre pedidos no satisfechos y calculando el total de unidades faltantes.

5. Selección de Columnas

def select_columns(df, columns):
    """Selecciona un subconjunto de columnas de un DataFrame."""

Selecciona un subconjunto de columnas de un DataFrame, asegurando que todas las columnas solicitadas existan.

6. Guardar Resultados en Excel

def save_to_excel(df, file_name):
    """Guarda un DataFrame en un archivo Excel."""

Guarda un DataFrame en un archivo Excel, manejando posibles errores durante el proceso.

Flujo Principal de Ejecución
Carga los archivos de pedidos y stock.
Normaliza y mapea las columnas necesarias.
Filtra y asigna el stock según los pedidos.
Guarda los resultados en un archivo Excel.
