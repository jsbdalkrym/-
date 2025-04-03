# -
خلية حروف
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>خلية الحروف</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: orange;
            margin: 0;
        }
        .grid {
            display: flex;
            flex-wrap: wrap;
            width: 320px;
        }
        .cell {
            width: 50px;
            height: 50px;
            background-color: white;
            border: 2px solid black;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
            font-weight: bold;
            cursor: pointer;
            margin: 2px;
            clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
        }
        .cell.green {
            background-color: green;
            color: white;
        }
        .cell.orange {
            background-color: orange;
            color: black;
        }
    </style>
</head>
<body>

<div class="grid">
    <div class="cell">ب</div>
    <div class="cell">د</div>
    <div class="cell">و</div>
    <div class="cell">ص</div>
    <div class="cell">ق</div>
    <div class="cell">ث</div>
    <div class="cell">ه</div>
    <div class="cell">ض</div>
    <div class="cell">ي</div>
    <div class="cell">ح</div>
    <div class="cell">ك</div>
    <div class="cell">ط</div>
    <div class="cell">م</div>
    <div class="cell">ز</div>
    <div class="cell">ش</div>
    <div class="cell">ظ</div>
    <div class="cell">أ</div>
    <div class="cell">س</div>
    <div class="cell">ر</div>
    <div class="cell">ت</div>
    <div class="cell">ج</div>
    <div class="cell">غ</div>
    <div class="cell">ه</div>
    <div class="cell">ع</div>
    <div class="cell">ذ</div>
</div>

<script>
    document.querySelectorAll('.cell').forEach(cell => {
        cell.addEventListener('click', function() {
            if (this.classList.contains('green')) {
                this.classList.remove('green');
                this.classList.add('orange');
            } else if (this.classList.contains('orange')) {
                this.classList.remove('orange');
            } else {
                this.classList.add('green');
            }
        });
    });
</script>

</body>
</html>
