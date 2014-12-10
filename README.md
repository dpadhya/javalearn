javalearn
=========
//it is for simple login box with core java (Swing)

package virtual;

import java.awt.BorderLayout;
import java.awt.GridLayout;
import java.awt.event.ActionListener;
import javax.swing.*;
import java.awt.event.ActionEvent;

public class Virtual implements ActionListener {
JFrame economy;
    JPanel virtuPanel;
    int width = 30;
    int height = 30;
    JButton proceed;
    JLabel nombre, pass, confPass;
    JTextField name;
    JTextField password;
    JTextField confirmPass; 

    public Virtual(){
    economy = new JFrame("ECONOMY SIMULATOR");
    economy.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    virtuPanel = new JPanel(new GridLayout(height , width));
    formatIt();
    economy.getRootPane().setDefaultButton(proceed);
    economy.getContentPane().add(virtuPanel, BorderLayout.CENTER);
    economy.pack();     // ... having just added the panel to the window ...
    economy.setVisible(true);
    }
    public void formatIt() {
        nombre = new JLabel("Name:", SwingConstants.LEFT);
        pass = new JLabel("Password:", SwingConstants.LEFT);
        confPass = new JLabel("Confirm Password:", SwingConstants.LEFT);
        proceed = new JButton("Proceed to Bank Setup");
        proceed.addActionListener(this);     
        virtuPanel.add(nombre);
        name = new JTextField(40);
        nombre.setBorder(BorderFactory.createEmptyBorder(5,5,5,5));
        virtuPanel.add(pass);
        password = new JTextField(15);
        pass.setBorder(BorderFactory.createEmptyBorder(5,5,5,5));
        virtuPanel.add(confPass);
        confPass.setBorder(BorderFactory.createEmptyBorder(5,5,5,5));
        confirmPass = new JTextField(15);
        virtuPanel.add(proceed);
        confPass.setBorder(BorderFactory.createEmptyBorder(10,10,10,10));
        virtuPanel.add(name);
        virtuPanel.add(password);
        virtuPanel.add(confirmPass);
    }
    public void actionPerformed(ActionEvent event) { 

           String tempName = nombre.getText();
           String tempPass =  pass.getText();
           String tempconfirmPass =  confPass.getText();
     }

           private static void createAndShowGUI() {
               JFrame.setDefaultLookAndFeelDecorated(true);
               Virtual econ = new Virtual();        
     }

    public static void main(String[] args) {
        javax.swing.SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                createAndShowGUI();
            }
        });
    }
    
}

