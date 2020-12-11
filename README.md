import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JTextField;
import javax.swing.SwingConstants;
import java.awt.Color;
import java.awt.Font;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import java.awt.Component;
import javax.swing.JRadioButton;
import javax.swing.ButtonGroup;
import javax.swing.JLabel;

public class NiceCalculator {

	private JFrame frame;
	private JTextField textBox;
	double n1;
	double n2;
	double result;
	String Op;
	String Ans;
	private final ButtonGroup buttonGroup = new ButtonGroup();
	

	public static boolean isNumeric(String string) {
	    if (string == null) {
	        return false;
	    }
	    try {
	        double d = Double.parseDouble(string);
	    } catch (NumberFormatException nfe) {
	        return false;
	    }
	    return true;
	}
	
	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					NiceCalculator window = new NiceCalculator();
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
	public NiceCalculator() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.getContentPane().setFont(new Font("Tahoma", Font.PLAIN, 18));
		frame.getContentPane().setForeground(Color.GRAY);
		frame.getContentPane().setBackground(Color.DARK_GRAY);
		frame.setBounds(100, 100, 384, 574);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		textBox = new JTextField();
		textBox.setFont(new Font("Tahoma", Font.PLAIN, 20));
		textBox.setForeground(Color.BLACK);
		textBox.setBackground(Color.WHITE);
		textBox.setHorizontalAlignment(SwingConstants.RIGHT);
		textBox.setBounds(15, 11, 289, 48);
		frame.getContentPane().add(textBox);
		textBox.setColumns(10);
		textBox.setEditable(false);
		
		/// ROW 1
		JButton clearBtn = new JButton("Clear All");
		clearBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		clearBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				textBox.setText(null);
			}
		});
		
		clearBtn.setAlignmentX(Component.CENTER_ALIGNMENT);
		clearBtn.setBorder(null);
		clearBtn.setBounds(145, 179, 120, 23);
		frame.getContentPane().add(clearBtn);
		
		// ROW 2
		JButton sevenBtn = new JButton("7");
		sevenBtn.setBackground(Color.WHITE);
		sevenBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + sevenBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		sevenBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		sevenBtn.setBounds(15, 213, 70, 64);
		frame.getContentPane().add(sevenBtn);
		
		JButton eightBtn = new JButton("8");
		eightBtn.setBackground(Color.WHITE);
		eightBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + eightBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		eightBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		eightBtn.setBounds(100, 213, 75, 64);
		frame.getContentPane().add(eightBtn);
		
		JButton nineBtn = new JButton("9");
		nineBtn.setBackground(Color.WHITE);
		nineBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + nineBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		nineBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		nineBtn.setBounds(185, 213, 70, 64);
		frame.getContentPane().add(nineBtn);
		
		// ROW 3
		JButton fourBtn = new JButton("4");
		fourBtn.setBackground(Color.WHITE);
		fourBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + fourBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		fourBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		fourBtn.setBounds(15, 288, 70, 70);
		frame.getContentPane().add(fourBtn);
		
		JButton fiveBtn = new JButton("5");
		fiveBtn.setBackground(Color.WHITE);
		fiveBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + fiveBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		fiveBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		fiveBtn.setBounds(100, 288, 70, 70);
		frame.getContentPane().add(fiveBtn);
		
		JButton sixBtn = new JButton("6");
		sixBtn.setBackground(Color.WHITE);
		sixBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + sixBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		sixBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		sixBtn.setBounds(185, 288, 70, 70);
		frame.getContentPane().add(sixBtn);
		
		
		// ROW 4
		JButton oneBtn = new JButton("1");
		oneBtn.setBackground(Color.WHITE);
		oneBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + oneBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		oneBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		oneBtn.setBounds(15, 369, 70, 70);
		frame.getContentPane().add(oneBtn);
		
		JButton twoBtn = new JButton("2");
		twoBtn.setBackground(Color.WHITE);
		twoBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + twoBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		twoBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		twoBtn.setBounds(100, 369, 70, 70);
		frame.getContentPane().add(twoBtn);
		
		JButton threeBtn = new JButton("3");
		threeBtn.setBackground(Color.WHITE);
		threeBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + threeBtn.getText();
				textBox.setText(EnterNumber);
			}
		});
		threeBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		threeBtn.setBounds(185, 369, 70, 70);
		frame.getContentPane().add(threeBtn);
		
		
		// ROW 5
		JButton zeroBtn = new JButton("0");
		zeroBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textBox.getText() + zeroBtn.getText();
				textBox.setText(EnterNumber);
			}
			
		});
		zeroBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		zeroBtn.setBounds(100, 454, 70, 70);
		frame.getContentPane().add(zeroBtn);
		
	
		
		JButton pointBtn = new JButton(".");
		pointBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				textBox.setText(textBox.getText() + ".");
			}
			
		});
		
		pointBtn.setFont(new Font("Tahoma", Font.BOLD, 30));
		pointBtn.setBounds(185, 454, 70, 70);
		frame.getContentPane().add(pointBtn);
		
		JButton computeBtn = new JButton("Compute");
	
	
		computeBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				n2= Double.parseDouble(textBox.getText());
				if(Op == "+")
				{
					result = n1+n2;
					Ans = String.format("%.2f", result);
					textBox.setText(Ans);
					
				}
				if(Op == "-")
				{
					result = n1-n2;
					Ans = String.format("%.2f", result);
					textBox.setText(Ans);
					
				}
				if(Op == "*")
				{
					result = n1*n2;
					Ans = String.format("%.2f", result);
					textBox.setText(Ans);
					
				}
				if(Op == "/")
				{
					result = n1/n2;
					Ans = String.format("%.4f", result);
					textBox.setText(Ans);
					
				}
				
				
			}
		});
		computeBtn.setForeground(Color.BLACK);
		computeBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		computeBtn.setBounds(15, 179, 120, 23);
		frame.getContentPane().add(computeBtn);
		
		JRadioButton addBtn = new JRadioButton("Add");
		buttonGroup.add(addBtn);
		
		addBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				n1 = Double.parseDouble(textBox.getText());
				textBox.setText("");
				Op="+";
						
				

						
			}
		});
		addBtn.setBounds(25, 66, 109, 23);
		frame.getContentPane().add(addBtn);
		
		JRadioButton MultiBtn = new JRadioButton("Multiply");
		buttonGroup.add(MultiBtn);
		MultiBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				n1 = Double.parseDouble(textBox.getText());
				textBox.setText("");
				Op="*";
						
		
			
			}
		});
		MultiBtn.setBounds(185, 66, 109, 23);
		frame.getContentPane().add(MultiBtn);
		
		JRadioButton subtractBtn = new JRadioButton("Subtract");
		buttonGroup.add(subtractBtn);
		
		subtractBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				n1 = Double.parseDouble(textBox.getText());
				textBox.setText("");
				Op="-";
						
			}
		});
		subtractBtn.setBounds(26, 96, 109, 23);
		frame.getContentPane().add(subtractBtn);
		
		JRadioButton divideBtn = new JRadioButton("Divide");
		buttonGroup.add(divideBtn);
		
		divideBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				n1 = Double.parseDouble(textBox.getText());
				textBox.setText("");
				Op="/";
				
				
				
			}
		});
		
		JButton negativeBtn = new JButton("-");
		negativeBtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				double ops =Double.parseDouble(String.valueOf(textBox.getText()));
				ops = ops*(-1);
				textBox.setText(String.valueOf(ops));
				
			}
		});
		negativeBtn.setFont(new Font("Tahoma", Font.PLAIN, 20));
		negativeBtn.setBounds(15, 454, 70, 70);
		frame.getContentPane().add(negativeBtn);
		
		divideBtn.setBounds(185, 96, 109, 23);
		frame.getContentPane().add(divideBtn);
		
		JButton setABtn = new JButton("Set A");
		setABtn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
		
				
			}
		});
		setABtn.setBounds(25, 131, 89, 15);
		frame.getContentPane().add(setABtn);
		
		JButton setBBtn = new JButton("Set B");
		setBBtn.setBounds(25, 155, 89, 13);
		frame.getContentPane().add(setBBtn);
		
		JLabel aColon = new JLabel("A:");
		aColon.setForeground(Color.WHITE);
		aColon.setBounds(124, 131, 46, 14);
		frame.getContentPane().add(aColon);
		
		JLabel bColon = new JLabel("B:");
		bColon.setForeground(Color.WHITE);
		bColon.setBounds(124, 154, 29, 14);
		frame.getContentPane().add(bColon);
		
		JLabel labelA =  new JLabel("0.0");
		labelA.setForeground(Color.WHITE);
		textBox.setText("");
		labelA.setBounds(155, 131, 46, 14);
		frame.getContentPane().add(labelA);
		
		JLabel labelB = new JLabel("0.0");
		labelB.setForeground(Color.WHITE);
		textBox.setText("");
		labelB.setBounds(155, 154, 46, 14);
		frame.getContentPane().add(labelB);
		
	}
}
