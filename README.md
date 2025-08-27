<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>دانشگاه خاوران</title>
<style>
body {
    font-family: Tahoma, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}
header {
    background-color: #004080;
    color: white;
    padding: 15px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.menu {
    position: relative;
    cursor: pointer;
}
.menu-content {
    display: none;
    position: absolute;
    right: 0;
    background-color: white;
    color: black;
    min-width: 150px;
    box-shadow: 0px 4px 6px rgba(0,0,0,0.2);
    z-index: 1;
}
.menu-content a {
    display: block;
    padding: 10px 15px;
    text-decoration: none;
    color: black;
}
.menu-content a:hover {
    background-color: #f1f1f1;
}
.submenu {
    display: none;
    background-color: #eaeaea;
}
.submenu a {
    padding-left: 20px;
}
.page-title {
    text-align: center;
    margin: 20px;
    font-size: 20px;
}
.table-container {
    overflow-x: auto;
    margin: 0 10px 20px 10px;
}
table {
    width: 100%;
    border-collapse: collapse;
    min-width: 600px;
    background-color: white;
}
th, td {
    border: 1px solid #333;
    text-align: center;
    padding: 10px;
}
th {
    background-color: #004080;
    color: white;
}
@media (max-width: 500px) {
    .page-title {
        font-size: 18px;
    }
    th, td {
        padding: 8px;
        font-size: 14px;
    }
}
</style>
</head>
<body>

<header>
<div>دانشگاه خاوران</div>
<div class="menu" onclick="toggleMenu()">&#x22EE;
    <div class="menu-content" id="mainMenu">
        <a href="#" onclick="toggleSubmenu(event, 'education')">آموزش</a>
        <div class="submenu" id="education">
            <a href="#" onclick="openGrades(event)">نمرات ترم</a>
            <a href="#">برنامه کلاسی</a>
            <a href="#">انتخاب واحد</a>
            <a href="#">کارت ورود به جلسه</a>
        </div>
        <a href="#">شخصی</a>
    </div>
</div>
</header>

<div id="content">
<p style="text-align:center; margin-top:50px;">لطفاً گزینه‌ای از منو انتخاب کنید.</p>
</div>

<script>
function toggleMenu() {
    const menu = document.getElementById('mainMenu');
    menu.style.display = menu.style.display === 'block' ? 'none' : 'block';
}

function toggleSubmenu(event, id) {
    event.preventDefault();
    const submenu = document.getElementById(id);
    submenu.style.display = submenu.style.display === 'block' ? 'none' : 'block';
}

function openGrades(event) {
    event.preventDefault();
    const content = document.getElementById('content');
    content.innerHTML = `
        <div class="page-title">اطلاعیه نمرات ترم ۱۴۰۳_۱۴۰۴ نیمسال دوم</div>
        <div class="table-container">
        <table>
            <tr>
                <th>ردیف</th>
                <th>شماره درس</th>
                <th>نام درس</th>
                <th>واحد</th>
                <th>نام استاد</th>
                <th>نمره</th>
                <th>وضعیت نمره</th>
                <th>شماره نمره</th>
            </tr>
            <tr>
                <td>1</td>
                <td>116</td>
                <td>آیین زندگی_اخلاق کاربردی</td>
                <td>2</td>
                <td>محسن سعیدی فاضل</td>
                <td>19</td>
                <td>عادی</td>
                <td>10321030</td>
            </tr>
            <tr>
                <td>2</td>
                <td>122218</td>
                <td>نقشه برداری۱</td>
                <td>2</td>
                <td>محمد ابراهیم فاضل ولی پور</td>
                <td>17</td>
                <td>عادی</td>
                <td>10321155</td>
            </tr>
            <tr>
                <td>3</td>
                <td>122853</td>
                <td>فیزیک ۱</td>
                <td>3</td>
                <td>مهدی امیری دلوئی</td>
                <td>13</td>
                <td>عادی</td>
                <td>10321192</td>
            </tr>
            <tr>
                <td>4</td>
                <td>122855</td>
                <td>ریاضی عمومی۱</td>
                <td>4</td>
                <td>سید ناصر باشی ازغدی</td>
                <td>14</td>
                <td>عادی</td>
                <td>10321188</td>
            </tr>
        </table>
        </div>
    `;
}
</script>

</body>
</html># Khavaran-site
