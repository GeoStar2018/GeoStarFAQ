需求：按F11按键某空间进入全屏模式，按ESC推出

做法：
引用using System.Runtime.InteropServices;
加入WindowsAPI
[DllImport("user32.dll", SetLastError = true)]
static extern IntPtr SetParent(IntPtr hWndChild, IntPtr hWndNewParent);

//窗体keydown事件
//还需要注意其他细节，比如判断当前是否全屏
    `private void Form1_KeyDown(object sender, KeyEventArgs e)
        {
            if(e.KeyCode==Keys.F11)
            {
                    （需要全屏控件下面统称A）A.Dock = DockStyle.None;
                    A.Left = 0;
                    A.Top = 0;
                    A.Width = Screen.PrimaryScreen.Bounds.Width;
                    A.Height = Screen.PrimaryScreen.Bounds.Height;
		    //脱离parent.handle
                    SetParent(A.Handle, IntPtr.Zero);
            }
            if (e.KeyCode == Keys.Escape)
            {
                    A.Dock = DockStyle.Fill;
		    //重新绑定parent.handle
                    SetParent(A.Handle, this.panel.Handle);
            }
        }`