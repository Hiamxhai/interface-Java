# interface-Java
Full code build app
package hai;

import java.awt.Button;
import java.awt.Color;
import java.awt.Dimension;
import java.awt.FlowLayout;
import java.awt.Font;
import java.awt.TextField;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.Action;
import javax.swing.ButtonGroup;
import javax.swing.ImageIcon;
import javax.swing.JButton;
import javax.swing.JCheckBox;
import javax.swing.JFrame;
import javax.swing.JRadioButton;
import javax.swing.JTextField;

import org.w3c.dom.Text;

public class MyFrame extends JFrame implements ActionListener{
	
	JRadioButton pizzaButton;
	JRadioButton hamburgerButton;
	JRadioButton hotdogButton;
	ImageIcon hamburgerIcon;
	ImageIcon hotdogIcon;
	ImageIcon pizzaIcon;
	 MyFrame() {
		
		this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		this.setLayout(new FlowLayout());
		
		pizzaIcon = new ImageIcon("pizza.jfif");
		hotdogIcon = new ImageIcon("hotdog.jfif");
		hamburgerIcon = new ImageIcon("hamburger.jfif");
		
		
		JRadioButton pizzaButton = new JRadioButton("pizza");
		JRadioButton hamburgerButton = new JRadioButton("hamburger");
		JRadioButton hotdogButton = new JRadioButton("hotdog");
		
		ButtonGroup group = new ButtonGroup();
		group.add(pizzaButton);
		group.add(hotdogButton);
		group.add(hamburgerButton);
		
		pizzaButton.addActionListener(this);
		hamburgerButton.addActionListener(this);
		hotdogButton.addActionListener(this);
		
		pizzaButton.setIcon(pizzaIcon);
		hamburgerButton.setIcon(hamburgerIcon);
		hotdogButton.setIcon(hotdogIcon);
		
		this.add(pizzaButton);
		this.add(hamburgerButton);
		this.add(hotdogButton);
		this.pack();
		this.setVisible(true);
				
	}
	@Override
	public void actionPerformed(ActionEvent e) {
		if(e.getSource()==pizzaButton) {
			System.out.println("you odered pizza");
		}
		else if(e.getSource()==hamburgerButton) {
			System.out.println("you odered hamburger");
		}
		else if(e.getSource()==hotdogButton) {
			System.out.println("you odered hot dog");
		}
	}
	
}







