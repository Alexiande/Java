package ru.mirea.task11.opt2;

import javax.swing.*;
import java.awt.*;
import java.awt.event.MouseEvent;
import java.awt.event.MouseListener;

public class Task extends JFrame {
    Button north=new Button("NORTH");
    Button east=new Button("EAST");
    Button west=new Button("WEST");
    Button south=new Button("SOUTH");
    Button center=new Button("CENTER");

    Task()
    {
        super("window");
        setSize(500,500);
        setLayout(new BorderLayout());
        add(north,BorderLayout.NORTH);
        add(east,BorderLayout.EAST);
        add(west,BorderLayout.WEST);
        add(south,BorderLayout.SOUTH);
        add(center,BorderLayout.CENTER);
        MouseListener listener =new MouseListener() {
            @Override
            public void mouseClicked(MouseEvent e) {

            }

            @Override
            public void mousePressed(MouseEvent e) {

            }

            @Override
            public void mouseReleased(MouseEvent e) {

            }

            @Override
            public void mouseEntered(MouseEvent e) {
                Button source= (Button) e.getSource();
                if (north.equals(source)) {
                    JOptionPane.showMessageDialog(null, "Вы вошли на север");
                } else if (south.equals(source)) {
                    JOptionPane.showMessageDialog(null, "Вы вошли на юг");
                } else if (west.equals(source)) {
                    JOptionPane.showMessageDialog(null, "Вы вошли на запад");
                } else if (east.equals(source)) {
                    JOptionPane.showMessageDialog(null, "Вы вошли на восток");
                } else if (center.equals(source)) {
                    JOptionPane.showMessageDialog(null, "Вы вошли в центер");
                }

            }

            @Override
            public void mouseExited(MouseEvent e) {}
        };
        west.addMouseListener(listener);
        south.addMouseListener(listener);
        east.addMouseListener(listener);
        north.addMouseListener(listener);
        center.addMouseListener(listener);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }
    public static void main(String[]args)
    {
        new Task();
    }
}
