package ru.mirea.task11.opt3;

import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class Task extends JFrame {

    Task()
    {

        super("window");
        setPreferredSize(new Dimension(270, 225));
        setLayout(new FlowLayout());
        JTextField field=new JTextField(10);
        field.setFont(new Font("TimesRoman", Font.PLAIN, 20));
        JMenuBar menuBar=new JMenuBar();
        JMenu font=new JMenu("Font");
        JMenuItem timesRoman=new JMenuItem("Times new Roman");
        JMenuItem forte=new JMenuItem("Forte");
        JMenuItem castellar=new JMenuItem("Castellar");
        JMenu color=new JMenu("Color");
        JMenuItem red=new JMenuItem("Red");
        JMenuItem blue=new JMenuItem("Blue");
        JMenuItem green=new JMenuItem("Green");
        menuBar.add(color);
        menuBar.add(font);
        setJMenuBar(menuBar);
        color.add(red);
        color.add(blue);
        color.add(green);
        font.add(timesRoman);
        font.add(forte);
        font.add(castellar);
        ActionListener actionListener=new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                JMenuItem jMenuItem=(JMenuItem)e.getSource();
                if (red.equals(jMenuItem)) {
                    field.setForeground(Color.RED);
                } else if (blue.equals(jMenuItem)) {
                    field.setForeground(Color.BLUE);
                } else if (green.equals(jMenuItem)) {
                    field.setForeground(Color.GREEN);
                } else if (timesRoman.equals(jMenuItem)) {
                    field.setFont(new Font("Times new roman", Font.PLAIN, 20));
                } else if (castellar.equals(jMenuItem)) {
                    field.setFont(new Font("Castellar", Font.PLAIN, 20));
                } else if (forte.equals(jMenuItem)) {
                    field.setFont(new Font("Forte", Font.PLAIN, 20));
                }
            }
        };
        red.addActionListener(actionListener);
        green.addActionListener(actionListener);
        blue.addActionListener(actionListener);
        forte.addActionListener(actionListener);
        timesRoman.addActionListener(actionListener);
        castellar.addActionListener(actionListener);
        pack();
        add(field);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }
    public static void main(String[]args)
    {
        new Task();
    }
}
