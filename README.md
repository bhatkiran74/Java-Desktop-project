# Java-Desktop-project
java projects
package calculatorPro;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JTextField;
import javax.swing.JSeparator;
import javax.swing.JButton;
import java.awt.Font;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.SwingConstants;
import java.awt.Toolkit;

public class CalculatorPro {

	private JFrame frame;
	private JTextField textDisplay;
	double firstnum;
	double secondnum;
	double result;
	String operations;
	String answer;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					CalculatorPro window = new CalculatorPro();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public CalculatorPro() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.setIconImage(Toolkit.getDefaultToolkit().getImage("C:\\Users\\kiran\\eclipse-workspace\\CalculatorPro\\src\\calculator-icon.png"));
		frame.getContentPane().setFont(new Font("Ubuntu", Font.BOLD, 20));
		frame.setBounds(100, 100, 297, 335);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		textDisplay = new JTextField();
		textDisplay.setHorizontalAlignment(SwingConstants.RIGHT);
		textDisplay.setFont(new Font("Ubuntu", Font.BOLD, 30));
		textDisplay.setBounds(10, 11, 260, 42);
		frame.getContentPane().add(textDisplay);
		textDisplay.setColumns(10);
		
		JSeparator separator = new JSeparator();
		separator.setBounds(10, 64, 260, 2);
		frame.getContentPane().add(separator);
		
		//========== row 1st==============================
		JButton r1c1btn = new JButton("C");
		r1c1btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				textDisplay.setText(null);
			}
		});
		r1c1btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r1c1btn.setBounds(10, 77, 54, 40);
		frame.getContentPane().add(r1c1btn);
		
		JButton backspace = new JButton("\u003c");
		backspace.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				if(textDisplay.getText().length()>0)
					 {
					 String backspace = null;
					
					 StringBuilder strB = new StringBuilder(textDisplay.getText());
					 strB.deleteCharAt(textDisplay.getText().length()-1);
					 backspace = strB.toString();
					 textDisplay.setText(backspace);
					 }
			}
		});
		backspace.setFont(new Font("Ubuntu", Font.BOLD, 25));
		backspace.setBounds(80, 77, 54, 40);
		frame.getContentPane().add(backspace);
		
		JButton r1c3btn = new JButton("%");
		r1c3btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textDisplay.getText());
				textDisplay.setText("");
				operations = "%";
			}
		});
		r1c3btn.setFont(new Font("Ubuntu", Font.BOLD, 20));
		r1c3btn.setBounds(150, 77, 54, 40);
		frame.getContentPane().add(r1c3btn);
		
		JButton r1c4btn = new JButton("+");
		r1c4btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textDisplay.getText());
				textDisplay.setText("");
				operations = "+";
			}
		});
		r1c4btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r1c4btn.setBounds(220, 77, 54, 40);
		frame.getContentPane().add(r1c4btn);
		
		//========== row 2nd==============================
		JButton r2c1btn = new JButton("1");
		r2c1btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r2c1btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});	
		r2c1btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r2c1btn.setBounds(10, 120, 54, 40);
		frame.getContentPane().add(r2c1btn);
		
		JButton r2c2btn = new JButton("2");
		r2c2btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r2c2btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r2c2btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r2c2btn.setBounds(80, 120, 54, 40);
		frame.getContentPane().add(r2c2btn);
		
		JButton r2c3btn = new JButton("3");
		r2c3btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r2c3btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r2c3btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r2c3btn.setBounds(150, 120, 54, 40);
		frame.getContentPane().add(r2c3btn);
		
		JButton r2c4btn = new JButton("-");
		r2c4btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textDisplay.getText());
				textDisplay.setText("");
				operations = "-";
			}
		});
		r2c4btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r2c4btn.setBounds(220, 120, 54, 40);
		frame.getContentPane().add(r2c4btn);

		//========== row 3rd==============================
		JButton r3c1btn = new JButton("4");
		r3c1btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r3c1btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r3c1btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r3c1btn.setBounds(10, 163, 54, 40);
		frame.getContentPane().add(r3c1btn);
		
		JButton r3c2btn = new JButton("5");
		r3c2btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r3c2btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r3c2btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r3c2btn.setBounds(80, 163, 54, 40);
		frame.getContentPane().add(r3c2btn);
		
		JButton r3c3btn = new JButton("6");
		r3c3btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r3c3btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r3c3btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r3c3btn.setBounds(150, 163, 54, 40);
		frame.getContentPane().add(r3c3btn);
		
		JButton r3c4btn = new JButton("*");
		r3c4btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textDisplay.getText());
				textDisplay.setText("");
				operations = "*";
			}
		});
		r3c4btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r3c4btn.setBounds(220, 163, 54, 40);
		frame.getContentPane().add(r3c4btn);

		//========== row 4th==============================
		JButton r4c1btn = new JButton("7");
		r4c1btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r4c1btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r4c1btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r4c1btn.setBounds(10, 206, 54, 40);
		frame.getContentPane().add(r4c1btn);
		
		JButton r4c2btn = new JButton("8");
		r4c2btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r4c2btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r4c2btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r4c2btn.setBounds(80, 206, 54, 40);
		frame.getContentPane().add(r4c2btn);
		
		JButton r4c3btn = new JButton("9");
		r4c3btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r4c3btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r4c3btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r4c3btn.setBounds(150, 206, 54, 40);
		frame.getContentPane().add(r4c3btn);
		
		JButton r4c4btn = new JButton("/");
		r4c4btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textDisplay.getText());
				textDisplay.setText("");
				operations = "/";
			}
		});
		r4c4btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r4c4btn.setBounds(220, 206, 54, 40);
		frame.getContentPane().add(r4c4btn);

		//========== row 5th==============================
		JButton r5c1btn = new JButton("0");
		r5c1btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r5c1btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		
		r5c1btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r5c1btn.setBounds(10, 249, 54, 40);
		frame.getContentPane().add(r5c1btn);
		
		JButton r5c2btn = new JButton(".");
		r5c2btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String EnterValue = textDisplay.getText() + r5c2btn.getText();
				 textDisplay.setText(EnterValue);
			}
		});
		r5c2btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r5c2btn.setBounds(80, 249, 54, 40);
		frame.getContentPane().add(r5c2btn);
		
		JButton r5c3btn = new JButton("\u00b1");
		r5c3btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				double plusminus =
				Double.parseDouble(String.valueOf(textDisplay.getText()));
				plusminus = plusminus*(-1);
				textDisplay.setText(String.valueOf(plusminus));
			}
		});
		r5c3btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r5c3btn.setBounds(150, 249, 54, 40);
		frame.getContentPane().add(r5c3btn);
		
		JButton r5c4btn = new JButton("=");
		r5c4btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String answer;
				secondnum = Double.parseDouble(textDisplay.getText());
				
				if(operations == "+")
				{
					result = firstnum + secondnum;
					answer = String.format("%.2f", result);
					textDisplay.setText(answer);
				}
				else if(operations == "-")
				{
					result = firstnum - secondnum;
					answer = String.format("%.2f", result);
					textDisplay.setText(answer);
				}
				else if(operations == "*")
				{
					result = firstnum * secondnum;
					answer = String.format("%.2f", result);
					textDisplay.setText(answer);
				}
				else if(operations == "/")
				{
					result = firstnum / secondnum;
					answer = String.format("%.2f", result);
					textDisplay.setText(answer);
				}
				else if(operations == "%")
				{
					result = firstnum % secondnum;
					answer = String.format("%.2f", result);
					textDisplay.setText(answer);
				}
			}
		});
		r5c4btn.setFont(new Font("Ubuntu", Font.BOLD, 30));
		r5c4btn.setBounds(220, 249, 54, 40);
		frame.getContentPane().add(r5c4btn);
		
	}
}
