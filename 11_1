package ru.mirea.task11.opt1;

import javax.swing.*;
import java.awt.*;

public class Task extends JFrame{
    int key,tries;
    JButton tryButton=new JButton("Угадать");
    JLabel message=new JLabel("Угадайте число от 1 до 20. У вас есть 3 жизни.");
    JLabel title=new JLabel("Угадайте число");
    JTextField field=new JTextField(10);
    Task() {
        super("Window");
        key=(int)(Math.random()*20);
        tries=0;
        GridBagLayout gridBagLayout = new GridBagLayout();
        Container container = getContentPane();
        GridBagConstraints constraints = new GridBagConstraints();
        container.setComponentOrientation(ComponentOrientation.LEFT_TO_RIGHT);
        setLayout(gridBagLayout);
        constraints.fill = GridBagConstraints.VERTICAL;
        setSize(400, 200);
        constraints.gridy=0;
        constraints.weightx=1;
        constraints.weighty=1;
        constraints.gridx=1;
        container.add(title, constraints);
        constraints.gridy=1;
        container.add(message, constraints);
        constraints.gridy=2;
        container.add(tryButton, constraints);
        constraints.gridy=3;
        container.add(field, constraints);
        tryButton.addActionListener(ae -> {
            int number;
            try {
                number=Integer.parseInt(field.getText().trim());
                tries++;
                if (tries==3)
                {
                    title.setText("Вы проиграли! Попытки кончились!");
                    field.setVisible(false);
                    message.setVisible(false);
                    tryButton.setVisible(false);
                    title.setForeground(Color.RED);
                }
                if(number>key)
                {
                    message.setText("Ошибка. Число должно быть меньше. У вас осталось:"+(3-tries)+ "жизнь(и)");
                }
                else if(number<key)
                {
                    message.setText("Ошибка. Число должно быть больше. У вас осталось:"+(3-tries)+ "жизнь(и)");
                }
                else
                {
                    field.setVisible(false);
                    tryButton.setVisible(false);
                    title.setVisible(false);
                    message.setForeground(Color.RED);
                    message.setText("Вы победили! Молодец!");
                }
            }
            catch (Exception e)
            {
                JOptionPane.showMessageDialog(null,"Введите целочисленное число");
            }
        });
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }
    public static void main(String []args)
    {
        new Task();
    }
}
