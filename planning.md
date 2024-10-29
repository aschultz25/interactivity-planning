## Objects
**Square**
   - **Properties**:
   - Position: (x, y)
   - Size: width, height
   - Movement: dx (horizontal speed), dy (vertical speed)

**Ellipse**
  - **Properties**:
   - Center Position: (cx, cy)
   - Size: major axis (rx), minor axis (ry)
   - Movement: dx (horizontal speed), dy (vertical speed)

## Conditions for Touching
- The square's edges are defined by its position and size.
- eg. square.rightEdge = square.x + square.width
- The ellipse's boundaries are defined by its center and radii.
- eg. ellipse.rightEdge = ellipse.cx + ellipse.rx (c=center) (r=radii)
- distance formula to assess if distance between the edges of both shapes is less than or equal to zero.

### Touching Condition Logic
```javascript
If (square.rightEdge >= ellipse.leftEdge && 
    square.leftEdge <= ellipse.rightEdge && 
    square.bottomEdge >= ellipse.topEdge && 
    square.topEdge <= ellipse.bottomEdge) {
    // The objects are touching
}

##Behavior Upon Touching
When the square and ellipse touch, they will bounce off each other.

Swap the direction of their velocities:
- square.dx = -square.dx
- ellipse.dx = -ellipse.dx
Simulates bouncing affect, as both objects will move away from one another upon collision.


