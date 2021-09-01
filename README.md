# Microsoft Visiul Studio 2019
# linkprogram

using System;

using System.Collections.Generic;

using System.ComponentModel;

using System.Data;

using System.Drawing;

using System.Linq;

using System.Text;

using System.Threading.Tasks;

using System.Windows.Forms;


namespace linkprogram
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void textBox1_TextChanged(object sender, EventArgs e)
        {

        }

        private void button1_MouseClick(object sender, MouseEventArgs e)
        {
            string gırıs = textBox1.Text;
            string son = "www." + gırıs + ".com";
            if (gırıs.StartsWith("https://"))
            {
                System.Diagnostics.Process.Start("chrome", gırıs);
            }
            if (gırıs.StartsWith("http://"))
            {
                System.Diagnostics.Process.Start("chrome", gırıs);
            }
            if (textBox1.TextLength == 0)
            {
                MessageBox.Show("No empty links!");
            }

            else
            {
                System.Diagnostics.Process.Start("chrome", son);
            }
        }

        private void textBox1_KeyPress(object sender, KeyPressEventArgs e)
        {
            if ((int)e.KeyChar == 32)
            {
                e.Handled = true;
            }
        }

        private void button2_MouseClick(object sender, MouseEventArgs e)
        {
            textBox1.Clear();
        }
    }
}
