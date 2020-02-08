//Clase Practica1
import javax.swing.JFrame;
import javax.swing.*;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
public class Practica1 extends JFrame {

    public Practica1() {
        setTitle("PRACTICA1"); 
        setBounds(300,100,500,500);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        iniciarComponentes();
    }
    
    private void iniciarComponentes(){
        JPanel panel = new JPanel();
        this.getContentPane().add(panel);
        panel.setLayout(null);
        
        JLabel etiqueta = new JLabel("Nombre: Alexis Altamirano Garcia");
        JLabel etiqueta2 = new JLabel("N° Control: 171160138");
        JLabel etiqueta3 = new JLabel("Carrera: I.S.C.");
        etiqueta.setBounds(100,100,300,100);
        etiqueta2.setBounds(100,150,300,100);
        etiqueta3.setBounds(100,200,300,100);
        panel.add(etiqueta);
        panel.add(etiqueta2);
        panel.add(etiqueta3);
        
        JButton Boton = new JButton("Mensaje");
        Boton.setBounds(100,300,150,50);
        panel.add(Boton);
        
        ActionListener OyenteDeAccion = new ActionListener(){
            
            public  void actionPerformed(ActionEvent evento){
                Ventana nueva = new Ventana();
                nueva.setVisible(true);
            }
        };
        Boton.addActionListener(OyenteDeAccion);
    }
    
    public static void main (String[] args) {
        Practica1 Ventana = new Practica1();
        Ventana.setVisible(true);
   
}
   
   
    
}

//Clase Ventana 
import javax.swing.JFrame;
import javax.swing.*;
public class Ventana extends JFrame {

    public Ventana() {
        this.setSize(500,500);
        setTitle("Mensaje");
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        
        JPanel panel = new JPanel();
        this.getContentPane().add(panel);
        panel.setLayout(null);
        
        JLabel etiqueta = new JLabel("Dirección: Lagunilla");
        JLabel etiqueta2 = new JLabel("N° Telefono: 9585891002");
        JLabel etiqueta3 = new JLabel("Genero: Masculino");
        etiqueta.setBounds(100,100,300,100);
        etiqueta2.setBounds(100,150,300,100);
        etiqueta3.setBounds(100,200,300,100);
        panel.add(etiqueta);
        panel.add(etiqueta2);
        panel.add(etiqueta3);
    }
    
    
}
