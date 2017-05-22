# DXFRead
DXF Reader for Xojo

This is a Component for XOJO for Read and View DXF Autocad File Format
Are a non-definitive version.
Any outside help will ensure that this project can be completed
Entities that can be viewed without problem:
- Circle, Point, Line, Text, Mtext, Arc, Ellipse, xLine
Entities that can be viewed with restriction:
- Polyline, Spline, LWPolyline
  Drawed with line, arc, bezier curve ( not support planar, cubic or quadratic curve ).
  
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

Changes History
------------------------------------------------------------------------------------------------------------------------------------------
21 May 2017 : Add Canvas Double Buffers
            : Save drawing in JPG, TIFF, BMP, PNG, GIF format
            
22 May 2017 : Resolve ARC, ELLIPSE Arc quadrant rotation, now work fine. 
            : Add Z axis on any class for future implementation of 3D 
            : Now layer color mods works fine
            : Modify all layer controller
            : Adding xline entity
