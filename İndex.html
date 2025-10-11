<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ZAREX BEDAVA HESAPLAR 🎮🔏</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif; }
        body { background-color: #1a1a1a; color: white; }
        header { background: #2c3e50; padding: 20px; text-align: center; }
        .header-top { display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px; }
        .add-btn { background: #3498db; color: white; border: none; border-radius: 50%; width: 40px; height: 40px; font-size: 24px; cursor: pointer; margin-right: 20px; }
        nav { background: #34495e; padding: 15px; text-align: center; }
        nav a { color: white; margin: 0 15px; cursor: pointer; text-decoration: none; }
        .container { max-width: 1000px; margin: 20px auto; padding: 20px; background: #2c3e50; border-radius: 10px; }
        .page { display: none; text-align: center; padding: 20px; }
        #anasayfa { display: block; }
        .search-bar { margin: 20px 0; padding: 15px; }
        .search-input { width: 80%; max-width: 500px; padding: 12px 20px; border: none; border-radius: 25px; background: rgba(255,255,255,0.1); color: white; font-size: 16px; }
        .rainbow-bg { background: linear-gradient(45deg, #ff0000, #ff8000, #ffff00, #00ff00, #0080ff, #0000ff, #8000ff); background-size: 400% 400%; animation: rainbow 8s ease infinite; border-radius: 10px; padding: 30px; color: white; }
        @keyframes rainbow { 0% { background-position: 0% 50% } 50% { background-position: 100% 50% } 100% { background-position: 0% 50% } }
        .file-list { margin: 20px 0; }
        .file-item { background: rgba(255,255,255,0.1); border-radius: 10px; padding: 15px; margin: 10px 0; display: flex; align-items: center; justify-content: space-between; text-align: left; }
        .file-user { display: flex; align-items: center; gap: 10px; flex: 1; }
        .user-avatar { width: 40px; height: 40px; border-radius: 50%; object-fit: cover; }
        .user-name { font-weight: bold; }
        .owner-name { color: yellow; }
        .file-info { flex: 2; padding: 0 15px; }
        .file-description { color: #ccc; font-size: 14px; margin-top: 5px; }
        .download-btn { background: #27ae60; color: white; border: none; padding: 8px 15px; border-radius: 5px; cursor: pointer; }
        .upload-section { margin: 30px 0; }
        .upload-area { border: 2px dashed #3498db; border-radius: 10px; padding: 40px; margin: 20px 0; cursor: pointer; }
        .file-input { display: none; }
        .description-input { width: 80%; max-width: 500px; padding: 12px; border: none; border-radius: 10px; background: rgba(255,255,255,0.1); color: white; margin: 15px 0; font-size: 16px; }
        .description-box { margin-top: 30px; padding: 20px; background: rgba(255,255,255,0.1); border-radius: 10px; text-align: left; }
        input, button { padding: 10px; margin: 5px; border: none; border-radius: 5px; }
        input { background: white; color: black; }
        button { background: #3498db; color: white; cursor: pointer; }
        .submit-btn { background: #27ae60; color: white; padding: 12px 30px; font-size: 16px; margin-top: 15px; }
        .logout-modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.7); justify-content: center; align-items: center; }
        .modal-content { background: #2c3e50; padding: 30px; border-radius: 10px; text-align: center; }
        .selected-file { margin: 15px 0; padding: 10px; background: rgba(255,255,255,0.1); border-radius: 5px; }
        .welcome-text { font-size: 24px; font-weight: bold; margin: 10px 0; }
    </style>
    
    <script>
        // TÜM FONKSİYONLARI HEAD İÇİNDE TANIMLA - BU SAYEDE ERKEN YÜKLENİRLER
        function showPage(pageId) {
            console.log("Sayfa değiştiriliyor: " + pageId);
            
            // Giriş kontrolü - paylasim ve dosyalar sayfaları için
            if ((pageId === 'paylasim' || pageId === 'dosyalar') && !localStorage.getItem('currentUser')) {
                alert('Giriş yapmadan Sayfa açılmaz!');
                return;
            }
            
            var pages = document.getElementsByClassName('page');
            for (var i = 0; i < pages.length; i++) {
                pages[i].style.display = 'none';
            }
            var targetPage = document.getElementById(pageId);
            if (targetPage) {
                targetPage.style.display = 'block';
                
                if (pageId === 'paylasim') {
                    updateShareProfile();
                }
                
                if (pageId === 'dosyalar') {
                    updateFilesList();
                }
            } else {
                console.error("Sayfa bulunamadı: " + pageId);
            }
        }

        function showLogoutModal() {
            document.getElementById('logoutModal').style.display = 'flex';
        }

        function closeLogoutModal() {
            document.getElementById('logoutModal').style.display = 'none';
        }

        function confirmLogout() {
            logout();
            closeLogoutModal();
        }

        var selectedFile = null;

        function handleFileUpload(files) {
            if (files.length > 0) {
                selectedFile = files[0];
                document.getElementById('selectedFileInfo').style.display = 'block';
                document.getElementById('fileName').textContent = selectedFile.name;
                document.getElementById('fileSize').textContent = (selectedFile.size / 1024 / 1024).toFixed(2) + ' MB';
            }
        }

        function submitFile() {
            if (!selectedFile) {
                alert('Lütfen önce bir dosya seçin!');
                return;
            }
            
            if (!localStorage.getItem('currentUser')) {
                alert('Dosya paylaşmak için giriş yapmalısınız!');
                showPage('giris');
                return;
            }
            
            var description = document.getElementById('fileDescription').value || 'Açıklama yok';
            saveFileToStorage(selectedFile, description);
        }

        function saveFileToStorage(file, description) {
            var reader = new FileReader();
            reader.onload = function(e) {
                var fileData = {
                    name: file.name,
                    size: file.size,
                    type: file.type,
                    content: e.target.result,
                    description: description,
                    uploader: localStorage.getItem('currentUser'),
                    timestamp: new Date().toLocaleString('tr-TR'),
                    id: Date.now()
                };
                
                var files = JSON.parse(localStorage.getItem('sharedFiles') || '[]');
                files.unshift(fileData);
                localStorage.setItem('sharedFiles', JSON.stringify(files));
                
                alert('Dosya başarıyla paylaşıldı!');
                
                selectedFile = null;
                document.getElementById('fileDescription').value = '';
                document.getElementById('selectedFileInfo').style.display = 'none';
                document.getElementById('shareFile').value = '';
                
                showPage('dosyalar');
            };
            reader.readAsDataURL(file);
        }

        function updateFilesList() {
            console.log("Dosya listesi güncelleniyor...");
            var filesList = document.getElementById('filesList');
            filesList.innerHTML = '';
            
            var files = JSON.parse(localStorage.getItem('sharedFiles') || '[]');
            console.log("LocalStorage'dan alınan dosyalar:", files);
            
            if (files.length === 0) {
                filesList.innerHTML = '<p>Henüz hiç dosya paylaşılmamış.</p>';
                return;
            }
            
            files.forEach(function(file) {
                console.log("Dosya ekleniyor:", file.name);
                var fileItem = document.createElement('div');
                fileItem.className = 'file-item';
                fileItem.setAttribute('data-filename', file.name.toLowerCase());
                fileItem.setAttribute('data-description', file.description.toLowerCase());
                
                fileItem.innerHTML = `
                    <div class="file-user">
                        <span class="user-name ${file.uploader === 'Zarex_kadir' ? 'owner-name' : ''}">
                            ${file.uploader === 'Zarex_kadir' ? 'Zarex_kadir (🔑Owner)' : file.uploader}
                        </span>
                    </div>
                    <div class="file-info">
                        <strong>${file.name}</strong>
                        <div class="file-description">${file.description}</div>
                        <small>${(file.size / 1024).toFixed(2)} KB - ${file.timestamp}</small>
                    </div>
                    <button class="download-btn" onclick="downloadFile(${file.id})">İndir</button>
                `;
                
                filesList.appendChild(fileItem);
            });
        }

        function filterFiles() {
            var searchText = document.getElementById('searchInput').value.toLowerCase();
            var fileItems = document.querySelectorAll('.file-item');
            
            fileItems.forEach(function(item) {
                var fileName = item.getAttribute('data-filename');
                var fileDescription = item.getAttribute('data-description');
                
                if (fileName.includes(searchText) || fileDescription.includes(searchText)) {
                    item.style.display = 'flex';
                } else {
                    item.style.display = 'none';
                }
            });
        }

        function downloadFile(fileId) {
            var files = JSON.parse(localStorage.getItem('sharedFiles') || '[]');
            var file = files.find(f => f.id === fileId);
            
            if (file) {
                var link = document.createElement('a');
                link.href = file.content;
                link.download = file.name;
                link.click();
            } else {
                console.error("Dosya bulunamadı:", fileId);
            }
        }

        function updateShareProfile() {
            var currentUser = localStorage.getItem('currentUser');
            if (currentUser) {
                document.getElementById('shareUsername').textContent = 
                    currentUser === 'Zarex_kadir' ? 'Zarex_kadir (🔑Owner)' : currentUser;
            }
        }

        function register() {
            var user = document.getElementById('regUser').value;
            var pass = document.getElementById('regPass').value;
            var pass2 = document.getElementById('regPass2').value;
            var msg = document.getElementById('regMsg');
            
            if (!user || !pass || !pass2) {
                msg.innerHTML = 'Tüm alanları doldurun!';
                msg.style.color = 'red';
                return;
            }
            
            if (pass !== pass2) {
                msg.innerHTML = 'Şifreler uyuşmuyor!';
                msg.style.color = 'red';
                return;
            }
            
            var users = JSON.parse(localStorage.getItem('users') || '{}');
            if (users[user]) {
                msg.innerHTML = 'Bu kullanıcı adı alınmış!';
                msg.style.color = 'red';
                return;
            }
            
            users[user] = { password: pass };
            localStorage.setItem('users', JSON.stringify(users));
            
            msg.innerHTML = 'Kayıt başarılı! Giriş yapabilirsiniz.';
            msg.style.color = 'green';
            
            document.getElementById('regUser').value = '';
            document.getElementById('regPass').value = '';
            document.getElementById('regPass2').value = '';
        }

        function login() {
            var user = document.getElementById('loginUser').value;
            var pass = document.getElementById('loginPass').value;
            var msg = document.getElementById('loginMsg');
            
            if (!user || !pass) {
                msg.innerHTML = 'Tüm alanları doldurun!';
                msg.style.color = 'red';
                return;
            }
            
            var users = JSON.parse(localStorage.getItem('users') || '{}');
            if (users[user] && users[user].password === pass) {
                localStorage.setItem('currentUser', user);
                msg.innerHTML = 'Giriş başarılı!';
                msg.style.color = 'green';
                updateAuthUI();
                showPage('anasayfa');
            } else {
                msg.innerHTML = 'Kullanıcı adı veya şifre hatalı!';
                msg.style.color = 'red';
            }
        }

        function logout() {
            localStorage.removeItem('currentUser');
            updateAuthUI();
            showPage('anasayfa');
        }

        function updateAuthUI() {
            var currentUser = localStorage.getItem('currentUser');
            var authLinks = document.getElementById('authLinks');
            var profile = document.getElementById('profile');
            
            if (currentUser) {
                authLinks.style.display = 'none';
                profile.style.display = 'block';
                document.getElementById('userName').textContent = currentUser === 'Zarex_kadir' ? 'Zarex_kadir (🔑Owner)' : currentUser;
            } else {
                authLinks.style.display = 'block';
                profile.style.display = 'none';
            }
        }

        // Sayfa yüklendiğinde çalışacak kod
        document.addEventListener('DOMContentLoaded', function() {
            console.log("Sayfa yüklendi! Tüm fonksiyonlar hazır.");
            updateAuthUI();
            
            // Test kullanıcısı oluştur
            var users = JSON.parse(localStorage.getItem('users') || '{}');
            if (!users['test']) {
                users['test'] = { password: 'test123' };
                localStorage.setItem('users', JSON.stringify(users));
            }
            
            // Örnek dosya ekle (eğer yoksa)
            var files = JSON.parse(localStorage.getItem('sharedFiles') || '[]');
            if (files.length === 0) {
                var exampleFile = {
                    name: "Örnek Dosya.txt",
                    size: 1024,
                    type: "text/plain",
                    content: "data:text/plain;base64,VGhpcyBpcyBhbiBleGFtcGxlIGZpbGUu",
                    description: "Bu bir örnek dosyadır",
                    uploader: "Zarex_kadir",
                    timestamp: new Date().toLocaleString('tr-TR'),
                    id: Date.now()
                };
                files.push(exampleFile);
                localStorage.setItem('sharedFiles', JSON.stringify(files));
                console.log("Örnek dosya eklendi");
            }
            
            // İlk yüklemede dosya listesini göster
            updateFilesList();
        });
    </script>
</head>
<body>
    <div id="logoutModal" class="logout-modal">
        <div class="modal-content">
            <h3>Çıkış yapmak istediğinize emin misiniz? 🚪</h3>
            <div>
                <button onclick="confirmLogout()">Evet</button>
                <button onclick="closeLogoutModal()">Hayır</button>
            </div>
        </div>
    </div>

    <header>
        <div class="header-top">
            <button class="add-btn" onclick="showPage('paylasim')">+</button>
            <h1>ZAREX BEDAVA HESAPLAR 🎮🔏</h1>
            <div style="width: 40px;"></div>
        </div>
        <div class="welcome-text">ZAREX BEDAVA HESAPLARA HOŞGELDİNİZ! 👾</div>
        <div>Kurdish 🇹🇯 | Turkish 🇹🇷</div>
        
        <div id="authLinks">
            <span onclick="showPage('giris')">Giriş Yap</span>
            <span onclick="showPage('kayit')">Kayıt Ol</span>
        </div>
        
        <div id="profile" style="display:none">
            <span id="userName"></span>
            <button onclick="showLogoutModal()">Çıkış Yap</button>
        </div>
    </header>

    <nav>
        <span onclick="showPage('anasayfa')">Ana Sayfa</span>
        <span onclick="showPage('hakkinda')">Hakkında</span>
        <span onclick="showPage('dosyalar')">Dosyalar</span>
        <span onclick="showPage('sosyal')">Sosyal Medya</span>
    </nav>

    <div class="container">
        <div id="anasayfa" class="page">
            <h2>Ana Sayfa</h2>
            <p>Yakında yeni özellikler geliyor! 🚀</p>
        </div>

        <div id="hakkinda" class="page">
            <h2>Hakkında</h2>
            <p>ZAREX BEDAVA HESAPLAR! 🎮🔏</p>
        </div>

        <div id="dosyalar" class="page">
            <h2>📁 Paylaşılan Dosyalar</h2>
            
            <div class="search-bar">
                <input type="text" id="searchInput" class="search-input" placeholder="🔍 Dosya adı veya açıklamada ara..." onkeyup="filterFiles()">
            </div>
            
            <div class="description-box">
                <h3>Topluluk Paylaşımları</h3>
                <p>Arama çubuğunu kullanarak dosya adı veya açıklamalarda arama yapabilirsiniz.</p>
            </div>

            <div id="filesList" class="file-list"></div>
        </div>

        <div id="paylasim" class="page rainbow-bg">
            <h2>📤 Dosya Paylaş</h2>
            
            <div id="shareProfile" class="file-user" style="justify-content: center; margin-bottom: 20px;">
                <span id="shareUsername" class="user-name"></span>
            </div>

            <div class="upload-section">
                <div class="upload-area" onclick="document.getElementById('shareFile').click()">
                    <div>📎 Dosya Seçmek İçin Tıklayın</div>
                    <p>Resim, PDF, ZIP veya diğer dosya türlerini yükleyebilirsiniz</p>
                </div>
                <input type="file" id="shareFile" class="file-input" onchange="handleFileUpload(this.files)">
                
                <div id="selectedFileInfo" class="selected-file" style="display: none;">
                    <strong>Seçilen dosya:</strong> <span id="fileName"></span>
                    <br>
                    <strong>Boyut:</strong> <span id="fileSize"></span>
                </div>
                
                <input type="text" id="fileDescription" class="description-input" placeholder="📝 Dosya açıklaması ekleyin...">
                
                <button class="submit-btn" onclick="submitFile()">📤 GÖNDER</button>
            </div>

            <div class="description-box">
                <h3>📝 Dosya Paylaşım Kuralları</h3>
                <p>• Sadece yasal içerikler paylaşılabilir</p>
                <p>• Maksimum dosya boyutu: Sınırsız</p>
                <p>• Paylaştığınız dosyalar herkese açık olacaktır</p>
            </div>
        </div>

        <div id="sosyal" class="page">
            <h2>Sosyal Medya İletişim</h2>
            <p>Bana TikTok'tan ulaşabilirsiniz!</p>
            <a href="https://tiktok.com/@zarex_kadir" target="_blank" style="color: #00f2ea;">
                TikTok: @zarex_kadir
            </a>
        </div>

        <div id="giris" class="page">
            <h2>Giriş Yap</h2>
            <input type="text" id="loginUser" placeholder="Kullanıcı Adı"><br>
            <input type="password" id="loginPass" placeholder="Şifre"><br>
            <button onclick="login()">Giriş Yap</button>
            <div id="loginMsg"></div>
        </div>

        <div id="kayit" class="page">
            <h2>Kayıt Ol<
