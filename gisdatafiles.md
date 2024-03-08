# Data Formats used in GIS and Data Analytics

Geographic Information System (GIS) data comes in various file formats, each serving different purposes and used in different aspects of spatial data handling and analysis. These formats can broadly be categorized into vector and raster data types. Vector data represents geographic features as points, lines, and polygons, while raster data represents geographic features as a grid of cells or pixels, each with a specific value.

## Vector Formats:

1. **File Geodatabase (.gdb)**:
   - An ESRI proprietary format that stores GIS data as a folder of files.
   - Supports storing multiple feature classes (spatial tables), raster datasets, and attributes (non-spatial tables). It is more efficient and can handle large datasets better than shapefiles.
   - Offers advanced features like relationship classes, topology, and network datasets.

2. **GeoPackage (.gpkg)**:
   - An open format based on SQLite database, designed to store multiple types of spatial data and attributes in a single file.
   - Supported by a wide range of GIS software, making it a good option for data exchange and interoperability.
   - Includes capabilities for vector features, tile matrix sets, and attributes.
   - ArcGIS Pro and QGIS can read/write these files, making it a good alternative to Shapefiles

3. **Shapefile (.shp)**: 
   - Developed by ESRI as an open specification for data interoperability among ESRI and other GIS software products.
   - One shapefile can only store one "table" of point, line or polygon. 
   - Consists of a minimum of three files (.shp for shape format, .shx for shape index format, and .dbf for attribute format).
   - Widely used but has major limitations, such as a 2GB file size limit and lack of support for multiple types of features (points, lines, and polygons) in a single file.
   - Good for transferring data between systems, but is a best practice to avoid storing and analysing from a Shapefile. It is better to convert shapefiles to a File Geodatabase (if in ArcGIS Pro) or a GeoPackage (if in QGIS) for anything but data transfer.

4. **GeoJSON (.geojson)**:
   - A lightweight format based on JSON (JavaScript Object Notation), used for representing simple geographical features, along with their non-spatial attributes.
   - Easy to read and write, making it popular for web applications and services.
   - Supports points, lines, polygons, and multi-part collections of these types.

5. **KML/KMZ (.kml/.kmz)**:
   - Keyhole Markup Language (KML) is an XML notation for expressing geographic annotation and visualization within Internet-based maps and Earth browsers (e.g., Google Earth).
   - KMZ is a compressed version of KML files.
   - Commonly used for displaying geographic data in an Earth browser such as Google Earth.

## Raster Formats:

1. **GeoTIFF (.tif)**:
   - An extension of the TIFF file format with added metadata for georeferencing. It is widely supported and serves as a standard for interchange of raster imagery and gridded data.
   - Capable of storing multiple bands, making it suitable for multi-spectral satellite imagery and other types of environmental data.

2. **ERDAS IMAGINE (.img)**:
   - A raster data format used by the ERDAS IMAGINE software, a popular remote sensing application.
   - Supports various types of data, including satellite imagery, aerial photographs, and elevation data.

3. **NetCDF (.nc)**:
   - Stands for Network Common Data Form, used for storing multidimensional scientific data such as temperature, humidity, pressure, wind speed, and direction.
   - Widely used in the atmospheric and oceanographic sciences.

4. **Digital Elevation Models (DEM)**:
   - Represents the Earth's surface elevation data as a grid of squares, or as a triangular irregular network.
   - Common formats include USGS DEM (.dem), ASTER GDEM (.tif), and SRTM (.hgt).

GIS and Data Analytic professionals often encounter various file formats depending on the nature of their projects and the tools they use. Understanding the strengths and limitations of each format is crucial for efficient data management and analysis. For instance, when working with large datasets or needing advanced spatial analysis capabilities, formats like File Geodatabases might be preferred. For web mapping applications, formats like GeoJSON and GeoPackage are often favored due to their interoperability and ease of use with web technologies.

In addition to the specific GIS data file types, GIS professionals frequently work with various common data formats that are integral for data storage, management, and analysis. These formats are widely used across different software applications for tabular data, databases, and spreadsheets. Understanding these formats is crucial for data import/export, integration, and analysis within GIS projects.

## Common Data Formats:

1. **CSV (Comma-Separated Values) (.csv)**:
   - A simple, widely used text format for storing tabular data. Each line of the file represents a data record, with each field separated by a comma.
   - Easily readable and writable by humans and computers, supported by virtually all data processing software, including GIS systems.
   - Lacks advanced features like data types and multiple sheets but is excellent for simple lists of points or attribute tables.

2. **Microsoft Excel (.xlsx/.xls)**:
   - A spreadsheet file format used by Microsoft Excel, part of the Microsoft Office suite.
   - Supports complex features like multiple sheets, formulas, graphs, and formatting.
   - Widely used for data analysis, storage, and transfer. GIS software can often read and import data directly from Excel files, though spatial data usually needs to be joined to existing GIS layers based on a common attribute.

3. **Microsoft Access Database (.accdb/.mdb)**:
   - Database file formats used by Microsoft Access, a database management system that combines the relational Microsoft Jet Database Engine with a graphical user interface and software-development tools.
   - `.mdb` is the file extension for Access databases up to Access 2003, while `.accdb` is used from Access 2007 onwards.
   - Useful for managing complex databases with multiple tables, queries, forms, and reports. GIS software can query Access databases directly or import data from them.

4. **Text Files (.txt)**:
   - Simple text files can also be used to store data, typically delimited in some way (e.g., space, tab, comma) to separate values.
   - While not as structured as CSV files, they are flexible and can be used with custom delimiters or formats, especially when dealing with legacy data or simple data logging.

5. **JSON (JavaScript Object Notation) (.json)**:
   - A lightweight data-interchange format that is easy for humans to read and write, and easy for machines to parse and generate.
   - Commonly used in web applications for data exchange between clients and servers. In the context of GIS, JSON is often used for configuration files, web service payloads, and even spatial data through GeoJSON.

6. **XML (eXtensible Markup Language) (.xml)**:
   - A markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable.
   - Used for data exchange and storage, configuration files, and more. In GIS, XML formats are often used for metadata, spatial data exchange (like GML - Geography Markup Language), and configuration.

## Interoperability in GIS and Data Analytics:

The ability to work with these common data formats is crucial for GIS professionals, as spatial data projects often require the integration of non-spatial data, such as demographic information, business data, and other attributes, which are commonly stored in formats like Excel, CSV, or databases. GIS software typically provides tools and functionalities to import, export, and convert these common data formats to and from GIS-specific formats, enabling a seamless flow of data between different systems and applications.

Understanding how to manipulate these formats and integrate them with spatial data is key to effective GIS analysis, allowing professionals to enrich their spatial datasets with additional layers of information and conduct more comprehensive analyses.

In the realm of data analytics, particularly "Big Data" there are other formats you may encounter.

**Note Fleming's GSA and SDA programs focuse on structured data (data in tables), and does not cover big data and its formats beyond a basic introduction.**

### Big Data and Analytics Specific Formats:

1. **Parquet (.parquet)**:
   - A columnar storage file format optimized for use with Big Data processing frameworks like Apache Hadoop and analytics tools like Apache Spark.
   - Designed to be highly efficient in both storage and performance, supporting advanced nested data structures.
   - Ideal for handling very large datasets because it supports efficient compression and encoding schemes.

2. **Avro (.avro)**:
   - A row-based storage format developed within the Hadoop ecosystem, designed for serializing data that allows for rich data structures in a compact, fast, binary format.
   - It supports schema evolution, allowing you to update the schema used to write the data, while maintaining compatibility with older schemas.
   - Commonly used for data serialization in big data processing pipelines.

3. **ORC (Optimized Row Columnar) (.orc)**:
   - A type of columnar storage format that provides a highly efficient way to store Hive data.
   - Designed to optimize both the size and processing speed of data, supporting advanced optimization techniques such as predicate pushdown.
   - Often used in Hadoop ecosystem projects for storing large, streaming datasets.

4. **Feather (.feather)**:
   - A binary columnar data format optimized for use in analytics. It was developed as part of the Apache Arrow project and is designed for efficient data exchange between data analytics tools.
   - Supports interoperability between different data analysis languages, such as Python (pandas), R, and more, making it an excellent choice for cross-language data sharing.

5. **HDF5 (Hierarchical Data Format version 5) (.hdf5)**:
   - A file format and set of technologies designed to store and organize large amounts of numerical data.
   - Supports complex data types and is capable of storing a mix of complex, heterogeneous data in a single file. This includes metadata and arrays of multidimensional data.
   - Widely used in academia and industry for storing large datasets, such as satellite imagery, computational simulations, and genomics data.

