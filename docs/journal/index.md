5/18/22
Began work on bezier curve generation for use in path generation, python psudocode is as follows
uses python graphics library point for visualization

```python
def getLinerarInterp(p1, p2, t):
    x = ((1-t)*p1.getX())+(t*p2.getX());
    y = ((1-t)*p1.getY())+(t*p2.getY());

    return Point(x, y)


def getPoint(points, t):
    newPoints = []
    if(len(points) == 1):
        return points[0]

    for i in range(len(points)-1):
        newPoints.append(getLinerarInterp(points[i], points[i+1], t))
    return getPoint(newPoints, t)
``` 

This seems to be a very nice way of generating curves, plans for the future primarily include priorities as follows
1. Write 2 wheel odometry localization for actual bot testing of everything else
2. Continue to experiment with bezier curve generation to better the later development of automatic generation
3. Test different path following algorithms to determine the best for bezier curves, starting with pure pursuit
