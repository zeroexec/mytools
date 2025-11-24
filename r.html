<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cigarette Tracker - Dark Mode Card View</title>
    <script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-database.js"></script>
    <style>
        /* Palet Warna Dark Mode */
        :root {
            --bg-primary: #121212;       
            --bg-secondary: #1e1e1e;     
            --bg-card: #282828;          
            --text-primary: #ffffff;     
            --text-secondary: #bbbbbb;   
            --red-main: #cf6679;         
            --red-delete: #e91e63;       
            --blue-add: #03dac6;         
            --green-quick: #8dcb8d;      
            --amber-warn: #ffbb33;       
            --border-color: #3e3e3e;     
            --tag-bg: #333333;           
        }

        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            display: flex; 
            flex-direction: column; 
            align-items: center; 
            padding: 20px; 
            background-color: var(--bg-primary);
            color: var(--text-primary);
            position: relative;
        }

        /* Tombol Reset diposisikan fixed di pojok kanan atas */
        #resetButton {
            position: fixed; 
            top: 20px;
            right: 20px;
            z-index: 1000;
            padding: 8px 15px;
            background-color: var(--amber-warn);
            color: var(--bg-primary);
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
        #resetButton:hover { background-color: #cc9929; }

        h1, h2 { color: var(--text-primary); margin-top: 0; }

        .header-container {
            width: 100%;
            max-width: 750px;
            display: flex;
            justify-content: center;
            padding-top: 10px;
            margin-bottom: 20px;
        }

        .controls { 
            display: flex; 
            gap: 15px; 
            margin-bottom: 30px;
            padding: 15px;
            background-color: var(--bg-secondary);
            border-radius: 8px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.4);
        }
        #logCigarette { 
            padding: 15px 30px; 
            font-size: 18px; 
            cursor: pointer; 
            background-color: var(--red-main); 
            color: var(--bg-primary); 
            border: none; 
            border-radius: 8px; 
            font-weight: bold;
            transition: background-color 0.3s;
        }
        #logCigarette:hover { background-color: #b75767; }
        
        .history { 
            width: 90%;
            max-width: 750px; 
            max-height: 70vh;
            overflow-y: auto; 
            background-color: var(--bg-secondary); 
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.4);
        }
        #cigaretteList { list-style: none; padding: 0; }

        /* Style untuk setiap log sebagai Card */
        #cigaretteList li {
            background-color: var(--bg-card);
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 15px; 
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            border: 1px solid var(--border-color);
        }
        
        /* Kontainer untuk Tanggal dan Tombol Hapus */
        .log-header {
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            /* margin-bottom dihapus, diganti dengan margin di tags-container */
        }

        .log-time-delete {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .data-display { 
            font-weight: bold;
            color: var(--text-secondary); /* Ubah warna agar kontras dengan tag */
            font-size: 14px;
        }

        /* Tombol Hapus Individual */
        .delete-log-button {
            background-color: var(--red-delete);
            color: white;
            border: none;
            padding: 6px 10px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 12px;
            font-weight: bold;
            transition: background-color 0.2s;
        }
        .delete-log-button:hover { background-color: #c2185b; }

        /* Kontainer Tags (Posisi Baru) */
        .tags-container {
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            margin-top: 8px; /* Pemisah dari tanggal */
            margin-bottom: 10px; /* Pemisah dari input */
            padding-bottom: 8px;
            border-bottom: 1px dotted var(--border-color); /* Garis pemisah dari input */
        }
        .tag {
            display: inline-flex;
            align-items: center;
            background-color: var(--tag-bg);
            color: var(--text-primary);
            padding: 4px 10px;
            margin-right: 5px;
            margin-bottom: 5px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 500;
        }
        .tag-remove {
            cursor: pointer;
            margin-left: 8px;
            font-weight: bold;
            color: var(--red-main);
        }
        .edit-section {
            width: 100%;
            /* Border top dihapus karena sudah ada di tags-container */
            padding-top: 5px;
            margin-top: 0;
        }
        .edit-controls {
            display: flex;
            gap: 5px;
            margin-bottom: 10px;
        }
        .edit-controls input {
            padding: 8px;
            border-radius: 4px;
            font-size: 12px;
            flex-grow: 1;
            background-color: #333333;
            border: 1px solid var(--border-color);
            color: var(--text-primary);
        }
        .edit-controls button {
            padding: 8px 12px;
            border-radius: 4px;
            font-size: 12px;
            cursor: pointer;
            background-color: var(--blue-add);
            color: var(--bg-primary);
            border: none;
            font-weight: bold;
        }
        .quick-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 5px;
        }
        .quick-tag-button {
            background-color: var(--green-quick);
            color: var(--bg-primary);
            border: none;
            padding: 5px 10px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 12px;
            font-weight: bold;
            transition: background-color 0.2s;
        }
        .quick-tag-button:hover { background-color: #79a879; }

        /* Scrollbar untuk dark mode */
        .history::-webkit-scrollbar { width: 8px; }
        .history::-webkit-scrollbar-thumb { background: #555; border-radius: 10px; }
        .history::-webkit-scrollbar-thumb:hover { background: #777; }
    </style>
</head>
<body>

    <div class="header-container">
        <h1>Cigarette Tracker</h1>
    </div>

    <button id="resetButton">RESET ALL DATA</button>

    <div class="controls">
        <button id="logCigarette">LOG CIGARETTE (Record Time Only)</button>
    </div>

    <div class="history">
        <h2>Full History Log</h2>
        <ul id="cigaretteList">
            <li>Loading data...</li>
        </ul>
    </div>

    <script>
        // 1. Firebase Configuration (TIDAK BERUBAH)
        const firebaseConfig = {
            apiKey: "AIzaSyB-kiGFrRI3GMfW7DT2Dt7DmpDBsFNvkgE",
            authDomain: "mysite-98643.firebaseapp.com",
            databaseURL: "https://mysite-98643-default-rtdb.firebaseio.com",
            projectId: "mysite-98643",
            storageBucket: "mysite-98643.firebasestorage.app",
            messagingSenderId: "464510122157",
            appId: "1:464510122157:web:9b2e1a1ed7d197a6796e24"
        };

        // Initialize Firebase
        firebase.initializeApp(firebaseConfig);
        const database = firebase.database();
        const cigarettesRef = database.ref('cigarettes'); 
        const tagsRef = database.ref('tags'); 
        
        const logButton = document.getElementById('logCigarette');
        const cigaretteList = document.getElementById('cigaretteList');
        const resetButton = document.getElementById('resetButton');

        let loadedTags = {}; 

        // 2. Load Quick Tags from Firebase 
        tagsRef.on('value', (snapshot) => {
            loadedTags = snapshot.val() || {
                'stressed': 'Stressed',
                'after_meal': 'After Meal',
                'with_coffee': 'With Coffee',
                'calm': 'Calm',
                'bored': 'Bored'
            };
        });

        // 3. Helper: Normalisasi Teks
        function normalizeText(text) {
            return text.toLowerCase().trim().replace(/\s/g, '_').replace(/[^a-z0-9_]/g, '');
        }

        // 4. Function: Log Cigarette
        logButton.addEventListener('click', () => {
            const timestamp = new Date().toISOString(); 
            
            const cigaretteData = {
                timestamp: timestamp, 
                descriptions: {}, 
                createdAt: firebase.database.ServerValue.TIMESTAMP 
            };

            cigarettesRef.push(cigaretteData)
                .then(() => {
                    console.log("Cigarette time successfully logged.");
                })
                .catch((error) => {
                    alert("Gagal mencatat log. Periksa koneksi internet Anda atau aturan keamanan Firebase.");
                    console.error("Error logging data:", error);
                });
        });

        // 5. Function: Delete All Data
        resetButton.addEventListener('click', () => {
            const confirmation = window.confirm(
                "⚠️ HARD WARNING ⚠️\n\nApakah Anda yakin ingin menghapus SEMUA data rokok dan SEMUA tag kustom? Aksi ini tidak bisa dibatalkan!"
            );

            if (confirmation) {
                database.ref().set(null)
                    .then(() => {
                        alert("Semua data berhasil dihapus (RESET BERHASIL).");
                    })
                    .catch((error) => {
                        alert("Gagal menghapus data. Periksa izin tulis Firebase Anda.");
                        console.error("Error deleting data:", error);
                    });
            } else {
                alert("Penghapusan data dibatalkan.");
            }
        });
        
        // 6. Function: Add Tag
        function addTag(key, tagValue) {
            const trimmedValue = tagValue.trim();
            const normalizedTag = normalizeText(trimmedValue);
            
            if (!trimmedValue || normalizedTag === "") {
                // Tidak perlu alert jika kosong, fungsi Enter Key sudah dicek di onkeydown
                return; 
            }
            
            // 6a. Add Tag to the Log Entry
            const updatePath = `descriptions/${normalizedTag}`; 
            cigarettesRef.child(key).child(updatePath).set(trimmedValue)
                .catch((error) => console.error("Error updating log tag:", error)); 
            
            // 6b. Add Tag to the Global Quick Tags list (if new)
            tagsRef.child(normalizedTag).set(trimmedValue)
                .catch((error) => console.error("Error updating quick tag list:", error)); 
        }
        
        // 7. Function: Remove Tag
        function removeTag(key, tagKey) {
            cigarettesRef.child(key).child('descriptions').child(tagKey).remove()
                .catch((error) => {
                    alert("Gagal menghapus tag.");
                    console.error("Error removing tag:", error);
                });
        }

        // 8. Helper: Create Tag Element for Display
        function createTagElement(key, tagKey, tagValue) {
            const tagDiv = document.createElement('div');
            tagDiv.className = 'tag';
            tagDiv.textContent = tagValue;
            
            const removeSpan = document.createElement('span');
            removeSpan.className = 'tag-remove';
            removeSpan.textContent = 'x';
            removeSpan.onclick = (e) => {
                e.stopPropagation(); 
                removeTag(key, tagKey);
            };
            
            tagDiv.appendChild(removeSpan);
            return tagDiv;
        }

        // 9. Function: Delete Individual Log
        function deleteLog(key) {
            const confirmDelete = window.confirm("Apakah Anda yakin ingin menghapus log rokok ini?");
            if (confirmDelete) {
                cigarettesRef.child(key).remove()
                    .then(() => console.log("Log berhasil dihapus."))
                    .catch((error) => {
                        alert("Gagal menghapus log.");
                        console.error("Error deleting log:", error);
                    });
            }
        }

        // 10. Main Rendering Function
        function renderCigaretteList(snapshot) {
            cigaretteList.innerHTML = ''; 
            
            const records = [];
            snapshot.forEach((childSnapshot) => {
                const val = childSnapshot.val();
                records.push({
                    key: childSnapshot.key,
                    descriptions: val.descriptions || {}, 
                    timestamp: val.timestamp,
                    key: childSnapshot.key
                });
            });

            // Reverse order so the latest is on top
            records.reverse().forEach((record) => {
                const dateString = new Date(record.timestamp).toLocaleString('en-US', {
                    hour: '2-digit', minute: '2-digit', second: '2-digit', day: '2-digit', month: 'short'
                });
                
                const listItem = document.createElement('li');
                
                // ----------------------------------------------------
                // 1. Log Header (Tanggal dan Tombol Hapus)
                // ----------------------------------------------------
                const logHeader = document.createElement('div');
                logHeader.className = 'log-header';

                const logTimeDelete = document.createElement('div');
                logTimeDelete.className = 'log-time-delete';

                const dataDisplay = document.createElement('span');
                dataDisplay.className = 'data-display';
                dataDisplay.textContent = `Log Time: ${dateString}`;
                logTimeDelete.appendChild(dataDisplay);

                // Tombol Hapus Individual
                const deleteLogButton = document.createElement('button');
                deleteLogButton.textContent = 'Hapus Log';
                deleteLogButton.className = 'delete-log-button';
                deleteLogButton.onclick = () => deleteLog(record.key);
                logTimeDelete.appendChild(deleteLogButton);

                logHeader.appendChild(logTimeDelete);
                listItem.appendChild(logHeader);

                // ----------------------------------------------------
                // 2. Tags Display Container (Posisi Baru: Di bawah Tanggal)
                // ----------------------------------------------------
                const tagsContainer = document.createElement('div');
                tagsContainer.className = 'tags-container';
                
                // Display Descriptions (Tags)
                Object.keys(record.descriptions).forEach(tagKey => {
                    const tagValue = record.descriptions[tagKey];
                    tagsContainer.appendChild(createTagElement(record.key, tagKey, tagValue));
                });
                listItem.appendChild(tagsContainer);
                
                // ----------------------------------------------------
                // 3. Edit Section (Input & Quick Buttons)
                // ----------------------------------------------------
                const editSection = document.createElement('div');
                editSection.className = 'edit-section';
                
                // Input and Add Button
                const editControls = document.createElement('div');
                editControls.className = 'edit-controls';

                const descriptionInput = document.createElement('input');
                descriptionInput.type = 'text';
                descriptionInput.placeholder = 'Ketik Tag (Lalu Enter/Click Add)';
                
                // 3a. Auto Capitalization (Kapitalisasi Otomatis Depan)
                descriptionInput.oninput = function() {
                    let val = this.value;
                    if (val.length > 0) {
                        // Hanya karakter pertama yang diubah menjadi uppercase
                        this.value = val.charAt(0).toUpperCase() + val.slice(1).toLowerCase();
                    }
                };

                // 3b. Enter Key Press Handler
                descriptionInput.onkeydown = (event) => {
                    if (event.key === 'Enter') {
                        event.preventDefault(); // Mencegah form submission/newline
                        addTag(record.key, descriptionInput.value);
                        descriptionInput.value = ''; // Bersihkan input
                    }
                };

                const addTagButton = document.createElement('button');
                addTagButton.textContent = 'Add Tag';
                addTagButton.onclick = () => {
                    addTag(record.key, descriptionInput.value);
                    descriptionInput.value = ''; // Bersihkan input
                };
                
                editControls.appendChild(descriptionInput);
                editControls.appendChild(addTagButton);
                editSection.appendChild(editControls);

                // Quick Tag Buttons
                const quickTagsDiv = document.createElement('div');
                quickTagsDiv.className = 'quick-tags';
                
                const sortedTagKeys = Object.keys(loadedTags).sort((a, b) => loadedTags[a].localeCompare(loadedTags[b]));

                // Buat tombol untuk setiap tag
                sortedTagKeys.forEach(tagKey => {
                    const tagValue = loadedTags[tagKey];
                    const quickButton = document.createElement('button');
                    quickButton.className = 'quick-tag-button';
                    quickButton.textContent = tagValue;
                    quickButton.onclick = () => {
                        addTag(record.key, tagValue);
                    };
                    quickTagsDiv.appendChild(quickButton);
                });
                
                editSection.appendChild(quickTagsDiv);
                listItem.appendChild(editSection);
                
                cigaretteList.appendChild(listItem);
            });

            if (records.length === 0) {
                cigaretteList.innerHTML = '<li>Belum ada data rokok yang dicatat.</li>';
            }
        }

        // 11. Listen for real-time changes
        cigarettesRef.orderByChild('createdAt').on('value', renderCigaretteList);
    </script>
</body>
</html>
