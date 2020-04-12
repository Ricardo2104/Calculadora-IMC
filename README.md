using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace CalcularIMC
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void btnCalcular_Click(object sender, EventArgs e)
        {
            float peso = float.Parse(txtPeso.Text);
            float altura = float.Parse(txtAltura.Text);
            float imc = peso / (altura * altura);
            
            if (imc < 18)
            {
                MessageBox.Show("Seu peso é: " + Math.Round(imc, 2) + " e você está abaixo do peso");
            }else if (imc < 25)
            {
                MessageBox.Show("Seu peso é: " + Math.Round(imc, 2) + " e você está com o peso normal");
            }else if (imc < 30)
            {
                MessageBox.Show("Seu peso é: " + Math.Round(imc, 2) + " e você está acima do peso");
            }else
            {
                MessageBox.Show("Seu peso é: " + Math.Round(imc, 2) + " e você está com obesidade morbida");
            }
        }
    }
}
