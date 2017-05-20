# DXFRead
DXF Reader for Xojo

This is a Component for XOJO for Read and View DXF Autocad File Format
Are a non-definitive version.
Any outside help will ensure that this project can be completed
Entities that can be viewed without problem:
- Circle, Point, Line, Text
Entities that can be viewed with restriction:
- Polyline, Spline, LWPolyline
  Drawed with line, arc, bezier curve ( not support planar, cubic or quadratic curve ).
- Arc, Elipse
  Problem with rotation arc

How does it work:
1. The DXF file is read and inserted into an array of text type classes called 'ENTITA'
   - Use DXF_Read(filedxf as folderitem) for start DXF READ also U can use DXF_ReadText(elencoentita as text) for passing a plain DXF text   
     as variable or stored in database
2. First Parsing locate the position of layer, block and entities
3. Open Layer parser and retrieve it
4. Skip Block parser for now ********
5. Open Entities parser
   5.1 Count and find position for all type of entities ( circle, line, point, arc, pline etc )
   5.2 Create a new class one for any entities
6. Determinate drawn extends
7. Draw all entities

Fired event DXF_redrawed when drawing complete
