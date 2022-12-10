    After defining 'create_line_geom(points)' (At "2: Create a function called create_line_geom()..."), the first assert, ..."Input should be a list", is triggered.
I get the error, "TypeError: 'list' object is not callable".  I wasn't sure if I should validate the assert list with '[]' (l = [] / type(points) == l, 
"Input should be a list") within the defined function, or I assigned the two Points in line1 in error:

def create_line_geom(points):
    l = []
    type(points) == l, "Input should be a list"
    assert len(points) >= 2, "LineString object requires at least two Points"
    assert print(points) == 'shapely.geometry.point.Point', "All List values should be Shapely Point objects!"
    return LineString(points)

line1 = Point(45.2, 22.34), Point(100.22, -3.20)

create_line_geom(line1)    
    
    
The following exerpts provide advice on composing the assert list part of the 'create_line_geom()' function:

(1) Inside the function, you should first check with assert -functionality that the input is a list (see lesson 6 from the Geo-Python course and hints for this exercise).
If something else than a list is passed for the function, you should return an Error message: "Input should be a list!"

(2) The lesson that the exercise is derived from:  https://autogis-site.readthedocs.io/en/latest/lessons/lesson-1/geometry-objects.html

(3) The background on assert:  https://geo-python-site.readthedocs.io/en/latest/notebooks/L6/gcp-5-assertions.html
