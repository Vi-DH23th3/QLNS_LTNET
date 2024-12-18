# QLNS_LTNET
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace quanlynhansach
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        //Hàm đăng nhập
        private void btnOK_Click(object sender, EventArgs e)
        {
            if ((this.txtTenDN.Text == "admin") && (this.txtMK.Text == "123"))
            {
                MessageBox.Show("Đăng nhập thành công", "Thông báo");
                this.Hide(); //ẩn form1
                Form2 f2 = new Form2();
                f2.ShowDialog();
            }
            else
            {
                MessageBox.Show("Tên và mật khẩu không đúng", "Thông báo");
                this.txtTenDN.Clear();
                this.txtMK.Clear();
                this.txtTenDN.Focus();

            }
        }
        // Button thoát
        private void btnCancel_Click(object sender, EventArgs e)
        {
            Application.Exit();
        }
    }
}
