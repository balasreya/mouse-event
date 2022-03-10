# mouse-event
import java.awt.*;
import java.awt.event.*;
import java.applet.*;


/*
<applet code="mouse_event" width=250 height=150>
</applet>
*/


public class mouse_event extends Applet implements MouseListener, MouseMotionListener 

{

String msg = " ";
int Mousex=0,Mousey=0;
public void init()
{
addMouseListener(this);
addMouseMotionListener(this);
}
public void mouseClicked(MouseEvent me)
{
Mousex=me.getX();
Mousey=me.getY();
msg="mouse Clicked";
repaint();
}
public void mouseEntered(MouseEvent me)
{
Mousex=me.getX();
Mousey=me.getY();
msg="mouse Entered";
repaint();
}
public void mouseExited(MouseEvent me)
{
Mousex=me.getX();
Mousey=me.getY();
msg="mouse Existed";
repaint();
}
public void mousePressed(MouseEvent me)
{
Mousex=me.getX();
Mousey=me.getY();
msg="down";
}
public void mouseReleased(MouseEvent me)
{
Mousex=me.getX();
Mousey=me.getY();
msg="Up";
repaint();
}
public void mouseDragged(MouseEvent me)
{
Mousex=me.getX();
Mousey=me.getY();
msg="*";
showStatus("dragging mouse at"+Mousex+";"+Mousey);
repaint();
}
public void mouseMoved(MouseEvent me)
{
showStatus("mouse movesst"+me.getX()+";"+me.getY());
}

public void paint(Graphics g)
{
setBackground(Color.blue);
setForeground(Color.red);
g.drawString(msg,Mousex,Mousey);
}
}

