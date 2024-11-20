# web_bot.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <title>Добавление продукта</title>
</head>
<body>
    <h3>Введите данные о продукте</h3>
    <form id="productForm">
        <label for="name">Название продукта:</label>
        <input type="text" id="name" name="name" required><br><br>
        <label for="calories">Калорийность (ккал):</label>
        <input type="number" id="calories" name="calories" required><br><br>
        <label for="proteins">Белки (г):</label>
        <input type="number" id="proteins" name="proteins" required><br><br>
        <label for="fats">Жиры (г):</label>
        <input type="number" id="fats" name="fats" required><br><br>
        <label for="carbs">Углеводы (г):</label>
        <input type="number" id="carbs" name="carbs" required><br><br>
        <label for="sugar">Сахар (г):</label>
        <input type="number" id="sugar" name="sugar" required><br><br>
        <label for="glycemic_index">Гликемический индекс:</label>
        <input type="number" id="glycemic_index" name="glycemic_index" required><br><br>
        <label for="insulin_index">Инсулиновый индекс:</label>
        <input type="number" id="insulin_index" name="insulin_index" required><br><br>
        <button type="button" onclick="submitForm()">Отправить</button>
    </form>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script>
        function submitForm() {
            const data = {
                name: document.getElementById('name').value,
                calories: document.getElementById('calories').value,
                proteins: document.getElementById('proteins').value,
                fats: document.getElementById('fats').value,
                carbs: document.getElementById('carbs').value,
                sugar: document.getElementById('sugar').value,
                glycemic_index: document.getElementById('glycemic_index').value,
                insulin_index: document.getElementById('insulin_index').value,
                };
            Telegram.WebApp.sendData(JSON.stringify(data));//Отправка данных в бот
                }
</script>
</body>
</html>
