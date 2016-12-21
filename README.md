# tfpdf
PHP 生成PDF文件

只是简单的把tFPDF 1.2.4包装成composer规范

# 用法
use tfpdf\Pdf;

$pdfLibrary = new Pdf();
$pdfLibrary->AddPage();
 
$pdfLibrary->image('http://img10.360buyimg.com/n0/g14/M02/00/05/rBEhVVKBuHAIAAAAAAHGc743SCcAAFhpwP9GxsAAcaL931.jpg',
       10,10,30,46,'JPG');
 
// Add a Unicode font (uses UTF-8)
$pdfLibrary->AddFont('Yahei','','Monaco_Yahei.ttf',true);
$pdfLibrary->SetFont('Yahei','',8);
 
$pdfLibrary->Write(8, "中文测试");
$pdfLibrary->Output('abc.pdf','D');


