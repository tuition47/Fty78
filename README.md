index.html

<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="سایت مدرن و واکنش‌گرا با حالت تاریک" />
  <title>سایت مدرن من</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-white text-gray-900 dark:bg-gray-900 dark:text-white transition-colors duration-300">

  <!-- Header -->
  <header class="bg-gray-100 dark:bg-gray-800 shadow-md sticky top-0 z-50">
    <nav class="max-w-6xl mx-auto flex items-center justify-between p-4">
      <div class="text-xl font-bold">لوگو</div>
      <ul class="flex gap-6">
        <li><a href="#" class="hover:text-blue-500">خانه</a></li>
        <li><a href="#about" class="hover:text-blue-500">درباره ما</a></li>
        <li><a href="#contact" class="hover:text-blue-500">تماس</a></li>
      </ul>
      <button id="toggleDark" class="p-2 bg-gray-300 dark:bg-gray-700 rounded-full">تاریک/روشن</button>
    </nav>
  </header>

  <!-- Main -->
  <main class="max-w-6xl mx-auto p-4 space-y-20">

    <!-- Hero -->
    <section class="text-center py-20">
      <h1 class="text-4xl font-extrabold mb-4">به سایت مدرن من خوش آمدید</h1>
      <p class="text-lg mb-6">ساخته‌شده با Tailwind CSS و حالت تاریک</p>
      <a href="#contact" class="px-6 py-3 bg-blue-600 text-white rounded-xl hover:bg-blue-700">ارتباط با ما</a>
    </section>

    <!-- About -->
    <section id="about" class="space-y-4">
      <h2 class="text-2xl font-bold">درباره ما</h2>
      <p>ما یک تیم طراحی و توسعه هستیم که عاشق ساخت وب‌سایت‌های سریع، سبک و زیبا هستیم. هدف ما ارائه تجربه‌ای ساده ولی حرفه‌ای برای کاربران است.</p>
    </section>

    <!-- Contact -->
    <section id="contact" class="space-y-6">
      <h2 class="text-2xl font-bold">ارتباط با ما</h2>
      <form class="grid grid-cols-1 md:grid-cols-2 gap-4" onsubmit="return validateForm()">
        <input type="text" id="name" placeholder="نام" required class="p-3 rounded border dark:bg-gray-800" />
        <input type="email" id="email" placeholder="ایمیل" required class="p-3 rounded border dark:bg-gray-800" />
        <textarea id="message" placeholder="پیام شما" rows="4" required class="p-3 rounded border md:col-span-2 dark:bg-gray-800"></textarea>
        <button type="submit" class="px-6 py-3 bg-green-600 text-white rounded-xl hover:bg-green-700 md:col-span-2">ارسال</button>
      </form>
    </section>

  </main>

  <!-- Footer -->
  <footer class="text-center py-6 bg-gray-200 dark:bg-gray-800 mt-20">
    <p>&copy; 2025 - ساخته شده با عشق</p>
  </footer>

  <!-- Script -->
  <script>
    document.getElementById('toggleDark').addEventListener('click', () => {
      document.documentElement.classList.toggle('dark');
    });

    function validateForm() {
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      const emailRegex = /^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$/;

      if (!name || !email || !message) {
        alert("لطفاً تمام فیلدها را پر کنید");
        return false;
      }

      if (!emailRegex.test(email)) {
        alert("ایمیل معتبر وارد کنید");
        return false;
      }

      alert("پیام شما با موفقیت ارسال شد!");
      return true;
    }
  </script>

</body>
</html>