问题描述：

C# ListView控件双击获取选中元素信息的方法

问题解答：

> private void listView1_MouseDoubleClick(object sender, MouseEventArgs e)
{
     ListViewHitTestInfo info = this.listView1.HitTest(e.X, e.Y);
     if(info.Item!=null)
     {
         int index = info.Item.Index;
     }
}