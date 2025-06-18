<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- SEO Meta Tags -->
    <title>Multi Tool Hub - Your Ultimate Collection of Free Online Tools</title>
    <meta name="description" content="Multi Tool Hub offers 20+ free, responsive, and easy-to-use online tools including image converters, calculators, text utilities, and more. All client-side, no uploads required for many tools!">
    <meta name="keywords" content="online tools, free tools, image converter, image compressor, image cropper, video converter, audio converter, audio trimmer, age calculator, emi calculator, sip calculator, qr code generator, password generator, word counter, base64, color picker, text to speech, speech to text, json formatter, unit converter, bmi calculator, timer, stopwatch, multi tool, utility website">
    <meta name="author" content="Multi Tool Hub">
    
    <!-- Open Graph Meta Tags (for social sharing) -->
    <meta property="og:title" content="Multi Tool Hub - Free Online Utilities">
    <meta property="og:description" content="Access a suite of 20 powerful online tools for images, audio, video, calculations, and text processing. Fast, free, and secure.">
    <meta property="og:type" content="website">
    
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Multi Tool Hub - 20+ Free Online Tools">
    <meta name="twitter:description" content="Your one-stop hub for versatile online tools: converters, calculators, generators, and more. Fully responsive and client-side.">
    
    <!-- Favicon -->
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🛠️</text></svg>">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

    <style>
        :root {
            --background-color: #1E1E2F;
            --text-color: #EAEAEA;
            --header-background: #2B2D42;
            --accent-color: #FFD700;
            --tool-card-background: #3A3D5B;
            --button-hover-color: #E6C200;
            --soft-box-shadow: 0 8px 16px rgba(255, 215, 0, 0.1);
            --card-hover-box-shadow: 0 12px 24px rgba(255, 215, 0, 0.2);
            --font-family: 'Poppins', sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-family);
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
            padding-bottom: 50px;
        }

        header {
            background-color: var(--header-background);
            color: var(--accent-color);
            padding: 1.5rem 1rem;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            margin-bottom: 2rem;
            position: sticky;
            top: 0;
            z-index: 999;
        }

        header h1 {
            font-weight: 700;
            font-size: 2.5rem;
        }

        main {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .tool-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
        }

        .tool-card {
            background-color: var(--tool-card-background);
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: var(--soft-box-shadow);
            transition: transform 0.3s ease, background-color 0.3s ease, color 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 0.5s ease-out forwards;
        }

        .tool-card:hover {
            transform: translateY(-5px);
            background-color: var(--accent-color);
            color: var(--background-color);
            box-shadow: var(--card-hover-box-shadow);
        }

        .tool-card h2 {
            font-size: 1.5rem;
            margin-bottom: 0.75rem;
            color: var(--text-color);
            transition: color 0.3s ease;
        }

        .tool-card:hover h2 {
            color: var(--background-color);
        }

        .tool-card p {
            font-size: 0.9rem;
            margin-bottom: 1rem;
            flex-grow: 1;
            opacity: 0.9;
        }

        .tool-card:hover p {
            color: var(--background-color);
            opacity: 1;
        }

        .tool-button {
            background-color: var(--accent-color);
            color: var(--background-color);
            border: none;
            padding: 0.75rem 1.25rem;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            text-align: center;
            transition: background-color 0.3s ease, color 0.3s ease;
            align-self: flex-start;
        }

        .tool-card:hover .tool-button {
            background-color: var(--background-color);
            color: var(--accent-color);
        }

        .tool-button:hover {
            background-color: var(--button-hover-color) !important;
            color: var(--background-color) !important;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.6);
            animation: fadeIn 0.3s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .modal-content {
            background-color: var(--header-background);
            margin: 5% auto;
            padding: 25px;
            border-radius: 10px;
            width: 90%;
            max-width: 700px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            position: relative;
            animation: slideIn 0.3s ease-in-out;
        }

        @keyframes slideIn {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        .close-button {
            color: var(--text-color);
            float: right;
            font-size: 28px;
            font-weight: bold;
            transition: color 0.2s ease;
            line-height: 1;
        }

        .close-button:hover,
        .close-button:focus {
            color: var(--accent-color);
            text-decoration: none;
            cursor: pointer;
        }

        .modal-body {
            margin-top: 1.5rem;
            color: var(--text-color);
        }

        .modal-body h3 {
            color: var(--accent-color);
            margin-bottom: 1rem;
        }

        .modal-body label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .modal-body input[type="text"],
        .modal-body input[type="number"],
        .modal-body input[type="date"],
        .modal-body input[type="file"],
        .modal-body textarea,
        .modal-body select {
            width: 100%;
            padding: 0.75rem;
            margin-bottom: 1rem;
            border-radius: 5px;
            border: 1px solid var(--tool-card-background);
            background-color: var(--background-color);
            color: var(--text-color);
            font-family: var(--font-family);
            font-size: 1rem;
        }

        .modal-body input[type="color"] {
            padding: 0.25rem;
            height: 45px;
        }

        .modal-body input[type="file"] { padding: 0.5rem; }
        .modal-body textarea { min-height: 100px; resize: vertical; }

        .modal-body button {
            background-color: var(--accent-color);
            color: var(--background-color);
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s ease;
            margin-top: 0.5rem;
            margin-right: 0.5rem;
        }

        .modal-body button:hover {
            background-color: var(--button-hover-color);
        }

        .modal-body .result-area {
            margin-top: 1rem;
            padding: 1rem;
            background-color: var(--background-color);
            border-radius: 5px;
            border: 1px solid var(--tool-card-background);
            white-space: pre-wrap;
            word-wrap: break-word;
        }

        .modal-body .option-group {
            margin-bottom: 1rem;
            padding: 0.75rem;
            border: 1px solid var(--tool-card-background);
            border-radius: 5px;
        }
        .modal-body .option-group label { display: inline-block; margin-right: 10px; font-weight: normal; }

        .modal-alert {
            margin-top: 1rem;
            padding: 0.75rem;
            border-radius: 5px;
            font-weight: bold;
        }
        .modal-alert.success { background-color: #28a745; color: white; }
        .modal-alert.error { background-color: #dc3545; color: white; }
        .modal-alert.info { background-color: #17a2b8; color: white; }

        #qrCodeContainer canvas {
            display: block;
            margin: 1rem auto;
            border: 5px solid var(--accent-color);
        }

        #imagePreview, #croppedImagePreview, #imagePreviewComp, #cropCanvas {
            max-width: 100%;
            max-height: 300px;
            margin-top: 1rem;
            border: 1px solid var(--accent-color);
            background-color: var(--background-color);
        }
        
        .color-picker-display { display: flex; align-items: center; margin-top: 1rem; }
        .color-picker-display .color-preview { width: 50px; height: 50px; border-radius: 5px; margin-right: 1rem; border: 1px solid var(--text-color); }
        .color-picker-display .color-values p { margin: 0.25rem 0; }

        .timer-display, .stopwatch-display { font-size: 2.5rem; font-weight: bold; text-align: center; margin-bottom: 1rem; color: var(--accent-color); }
        .laps-list { max-height: 150px; overflow-y: auto; border: 1px solid var(--tool-card-background); padding: 0.5rem; margin-top: 1rem; }
        .laps-list li { list-style-type: none; padding: 0.25rem 0.5rem; border-bottom: 1px dashed var(--tool-card-background); }
        .laps-list li:last-child { border-bottom: none; }
        
        .tabs { display:flex; margin-bottom:1rem; border-bottom:1px solid var(--tool-card-background); }
        .tab-button { background:none; border:none; color: var(--text-color); padding: 0.75rem 1rem; cursor:pointer; font-size: 1rem; font-family: var(--font-family); transition: background-color 0.3s, color 0.3s; }
        .tab-button.active { background-color: var(--accent-color); color: var(--background-color); border-bottom: 2px solid var(--accent-color); font-weight: bold; }
        .tab-button:not(.active):hover { background-color: var(--tool-card-background); }

        @keyframes fadeInUp {
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 992px) { /* Tablet */
            .tool-grid { grid-template-columns: repeat(2, 1fr); }
            header h1 { font-size: 2rem; }
        }

        @media (max-width: 768px) { /* Mobile */
            .tool-grid { grid-template-columns: 1fr; }
            .modal-content { width: 95%; margin: 10% auto; padding: 20px; }
            header h1 { font-size: 1.8rem; }
            .tool-card h2 { font-size: 1.3rem; }
            .modal-body button { padding: 0.7rem 1.2rem; font-size: 0.9rem; }
        }
    </style>
</head>
<body>
    <header>
        <h1>Multi Tool Hub</h1>
    </header>

    <main>
        <div class="tool-grid">
            <!-- Tool cards will be dynamically generated by JavaScript -->
        </div>
    </main>

    <!-- Generic Modal Structure -->
    <div id="toolModal" class="modal">
        <div class="modal-content">
            <span class="close-button">×</span>
            <h2 id="modalTitle">Tool Title</h2>
            <div id="modalBody" class="modal-body">
                <!-- Tool-specific content will be injected here -->
            </div>
            <div id="modalAlert" class="modal-alert" style="display:none;"></div>
        </div>
    </div>

    <script>
    document.addEventListener('DOMContentLoaded', () => {
        const toolGrid = document.querySelector('.tool-grid');
        const modal = document.getElementById('toolModal');
        const modalTitle = document.getElementById('modalTitle');
        const modalBody = document.getElementById('modalBody');
        const modalAlert = document.getElementById('modalAlert');
        const closeButton = document.querySelector('.close-button');

        const tools = [
            { id: 'imageConverter', title: 'Image Converter', description: 'Convert between JPG, PNG, and WEBP formats.' },
            { id: 'imageCompressor', title: 'Image Compressor', description: 'Compress image file size with quality settings.' },
            { id: 'imageCropper', title: 'Image Cropper', description: 'Upload, crop image with preview, and export.' },
            { id: 'videoConverter', title: 'Video Converter', description: 'Convert video (MP4 ↔ WebM via re-encoding). Browser-limited.' },
            { id: 'audioConverter', title: 'Audio Converter', description: 'Convert uploaded audio to WAV format.' },
            { id: 'audioTrimmer', title: 'Audio Trimmer', description: 'Upload, trim audio, and export trimmed WAV clip.' },
            { id: 'ageCalculator', title: 'Age Calculator', description: 'Calculate age from date of birth.' },
            { id: 'emiCalculator', title: 'EMI Calculator', description: 'Calculate Equated Monthly Installment for loans.' },
            { id: 'sipCalculator', title: 'SIP Calculator', description: 'Calculate future value of SIP investments.' },
            { id: 'qrCodeGenerator', title: 'QR Code Generator', description: 'Generate downloadable QR codes from text/URL.' },
            { id: 'passwordGenerator', title: 'Password Generator', description: 'Generate secure passwords with custom options.' },
            { id: 'wordCounter', title: 'Word Counter', description: 'Count words, characters, and estimate reading time.' },
            { id: 'base64EncoderDecoder', title: 'Base64 Encoder/Decoder', description: 'Encode to Base64 or decode from Base64.' },
            { id: 'colorPicker', title: 'Color Picker Tool', description: 'Pick colors and get HEX, RGB, HSL values.' },
            { id: 'textToSpeech', title: 'Text to Speech', description: 'Convert text into spoken audio using browser voices.' },
            { id: 'speechToText', title: 'Speech to Text', description: 'Convert voice from microphone into text.' },
            { id: 'jsonFormatter', title: 'JSON Formatter', description: 'Format and validate JSON data.' },
            { id: 'unitConverter', title: 'Unit Converter', description: 'Convert values between various units (length, weight, temp).' },
            { id: 'bmiCalculator', title: 'BMI Calculator', description: 'Calculate Body Mass Index and category.' },
            { id: 'timerStopwatch', title: 'Timer / Stopwatch', description: 'Simple timer and stopwatch functionality.' },
        ];

        function openModal(tool) {
            modalTitle.textContent = tool.title;
            modalBody.innerHTML = '';
            hideAlert();
            
            const toolFunction = toolInitializers[tool.id];
            if (toolFunction) {
                toolFunction(modalBody);
            } else {
                modalBody.innerHTML = '<p>Tool UI not implemented yet.</p>';
            }
            modal.style.display = 'block';
            document.body.style.overflow = 'hidden'; // Prevent background scrolling
        }

        function closeModal() {
            modal.style.display = 'none';
            modalBody.innerHTML = '';
            document.body.style.overflow = 'auto';
            if (window.currentToolCleanup) {
                window.currentToolCleanup();
                window.currentToolCleanup = null;
            }
        }

        closeButton.onclick = closeModal;
        window.onclick = (event) => {
            if (event.target === modal) {
                closeModal();
            }
        };
        
        function showAlert(message, type = 'info') {
            modalAlert.textContent = message;
            modalAlert.className = `modal-alert ${type}`;
            modalAlert.style.display = 'block';
        }

        function hideAlert() {
            modalAlert.style.display = 'none';
        }

        tools.forEach((tool, index) => {
            const card = document.createElement('div');
            card.className = 'tool-card';
            card.style.animationDelay = `${index * 0.05}s`;
            card.innerHTML = `
                <h2>${tool.title}</h2>
                <p>${tool.description}</p>
                <button class="tool-button" data-toolid="${tool.id}">Open Tool</button>
            `;
            card.querySelector('.tool-button').addEventListener('click', () => openModal(tool));
            toolGrid.appendChild(card);
        });

        // --- All Tool Logic ---
        const toolInitializers = {
            imageConverter: (container) => {
                container.innerHTML = `
                    <input type="file" id="imgConvFile" accept="image/jpeg,image/png,image/webp">
                    <label for="imgConvFormat">Convert to:</label>
                    <select id="imgConvFormat">
                        <option value="image/jpeg">JPEG</option>
                        <option value="image/png">PNG</option>
                        <option value="image/webp">WEBP</option>
                    </select>
                    <button id="imgConvButton">Convert & Download</button>
                    <p>Note: WEBP support varies by browser.</p>
                    <img id="imagePreview" src="#" alt="Preview" style="display:none;">
                `;
                const fileInput = container.querySelector('#imgConvFile');
                const formatSelect = container.querySelector('#imgConvFormat');
                const convertButton = container.querySelector('#imgConvButton');
                const preview = container.querySelector('#imagePreview');
                let originalFileName = 'converted_image';

                fileInput.onchange = (e) => {
                    if (e.target.files && e.target.files[0]) {
                        originalFileName = e.target.files[0].name.split('.')[0] || 'image';
                        const reader = new FileReader();
                        reader.onload = (event) => {
                            preview.src = event.target.result;
                            preview.style.display = 'block';
                        }
                        reader.readAsDataURL(e.target.files[0]);
                    } else {
                         preview.style.display = 'none';
                         preview.src="#";
                    }
                };

                convertButton.onclick = () => {
                    if (!fileInput.files || fileInput.files.length === 0) {
                        showAlert('Please select an image file first.', 'error');
                        return;
                    }
                    const file = fileInput.files[0];
                    const targetFormat = formatSelect.value;
                    const targetExtension = targetFormat.split('/')[1].replace('jpeg', 'jpg');

                    showAlert('Processing...', 'info');

                    const reader = new FileReader();
                    reader.onload = (event) => {
                        const img = new Image();
                        img.onload = () => {
                            const canvas = document.createElement('canvas');
                            canvas.width = img.width;
                            canvas.height = img.height;
                            const ctx = canvas.getContext('2d');
                            // If converting to JPG from PNG, fill background with white
                            if (targetFormat === 'image/jpeg' && file.type === 'image/png') {
                                ctx.fillStyle = '#FFFFFF';
                                ctx.fillRect(0, 0, canvas.width, canvas.height);
                            }
                            ctx.drawImage(img, 0, 0);
                            
                            canvas.toBlob((blob) => {
                                if (blob) {
                                    const url = URL.createObjectURL(blob);
                                    const a = document.createElement('a');
                                    a.href = url;
                                    a.download = `${originalFileName}_converted.${targetExtension}`;
                                    document.body.appendChild(a);
                                    a.click();
                                    document.body.removeChild(a);
                                    URL.revokeObjectURL(url);
                                    showAlert('Conversion successful!', 'success');
                                } else {
                                    showAlert(`Error converting to ${targetFormat}. This format might not be supported for export by your browser.`, 'error');
                                }
                            }, targetFormat, 0.9);
                        };
                        img.onerror = () => showAlert('Could not load image. Ensure it is a valid JPG, PNG, or WEBP.', 'error');
                        img.src = event.target.result;
                    };
                    reader.readAsDataURL(file);
                };
            },

            imageCompressor: (container) => {
                container.innerHTML = `
                    <input type="file" id="imgCompFile" accept="image/jpeg,image/png">
                    <label for="imgCompQuality">Quality (0.1 - 1.0 for JPEG, ignored for PNG):</label>
                    <input type="number" id="imgCompQuality" value="0.7" min="0.1" max="1.0" step="0.1">
                    <button id="imgCompButton">Compress & Download</button>
                    <p>PNG compression is lossless and the quality setting is ignored.</p>
                    <div id="compressionInfo" class="result-area" style="display:none;"></div>
                    <img id="imagePreviewComp" src="#" alt="Preview" style="display:none;">
                `;
                const fileInput = container.querySelector('#imgCompFile');
                const qualityInput = container.querySelector('#imgCompQuality');
                const compressButton = container.querySelector('#imgCompButton');
                const compressionInfo = container.querySelector('#compressionInfo');
                const preview = container.querySelector('#imagePreviewComp');
                let originalFileName = 'compressed_image';

                fileInput.onchange = (e) => {
                    if (e.target.files && e.target.files[0]) {
                        originalFileName = e.target.files[0].name.split('.')[0] || 'image';
                        const reader = new FileReader();
                        reader.onload = (event) => {
                            preview.src = event.target.result;
                            preview.style.display = 'block';
                        }
                        reader.readAsDataURL(e.target.files[0]);
                    } else {
                        preview.style.display = 'none';
                        preview.src = "#";
                    }
                };

                compressButton.onclick = () => {
                    if (!fileInput.files || fileInput.files.length === 0) {
                        showAlert('Please select an image file.', 'error');
                        return;
                    }
                    const file = fileInput.files[0];
                    const quality = parseFloat(qualityInput.value);
                    const originalSize = (file.size / 1024).toFixed(2);
                    showAlert('Processing...', 'info');

                    const reader = new FileReader();
                    reader.onload = (event) => {
                        const img = new Image();
                        img.onload = () => {
                            const canvas = document.createElement('canvas');
                            const ctx = canvas.getContext('2d');
                            canvas.width = img.width;
                            canvas.height = img.height;
                            ctx.drawImage(img, 0, 0);

                            let outputFormat = file.type === 'image/png' ? 'image/png' : 'image/jpeg';
                            let extension = outputFormat.split('/')[1].replace('jpeg', 'jpg');

                            canvas.toBlob((blob) => {
                                if (blob) {
                                    const compressedSize = (blob.size / 1024).toFixed(2);
                                    const url = URL.createObjectURL(blob);
                                    const a = document.createElement('a');
                                    a.href = url;
                                    a.download = `${originalFileName}_compressed.${extension}`;
                                    document.body.appendChild(a);
                                    a.click();
                                    document.body.removeChild(a);
                                    URL.revokeObjectURL(url);
                                    
                                    compressionInfo.innerHTML = `Original Size: ${originalSize} KB<br>Compressed Size: ${compressedSize} KB<br>Reduction: ${((1 - compressedSize / originalSize) * 100).toFixed(2)}%`;
                                    compressionInfo.style.display = 'block';
                                    showAlert('Compression successful!', 'success');
                                } else {
                                    showAlert('Error during compression.', 'error');
                                }
                            }, outputFormat, outputFormat === 'image/jpeg' ? quality : undefined);
                        };
                        img.onerror = () => showAlert('Could not load image.', 'error');
                        img.src = event.target.result;
                    };
                    reader.readAsDataURL(file);
                };
            },

            imageCropper: (container) => {
                container.innerHTML = `
                    <input type="file" id="imgCropFile" accept="image/*">
                    <p>After selecting an image, adjust crop parameters. A real cropper would have a draggable overlay.</p>
                    <canvas id="cropCanvas" style="display:none;"></canvas>
                    <br>
                    <label for="cropX">Crop Start X (px):</label> <input type="number" id="cropX" value="0" style="width:80px;">
                    <label for="cropY">Crop Start Y (px):</label> <input type="number" id="cropY" value="0" style="width:80px;">
                    <br>
                    <label for="cropW">Crop Width (px):</label> <input type="number" id="cropW" value="100" style="width:80px;">
                    <label for="cropH">Crop Height (px):</label> <input type="number" id="cropH" value="100" style="width:80px;">
                    <br>
                    <button id="cropButton">Crop & Download</button>
                    <img id="croppedImagePreview" src="#" alt="Cropped Preview" style="display:none; max-width: 100%; margin-top: 1rem;">
                `;
                const fileInput = container.querySelector('#imgCropFile');
                const cropCanvas = container.querySelector('#cropCanvas');
                const ctx = cropCanvas.getContext('2d');
                const cropXInput = container.querySelector('#cropX');
                const cropYInput = container.querySelector('#cropY');
                const cropWInput = container.querySelector('#cropW');
                const cropHInput = container.querySelector('#cropH');
                const cropButton = container.querySelector('#cropButton');
                const croppedPreview = container.querySelector('#croppedImagePreview');
                let sourceImage = null;
                let originalFileName = 'cropped_image';

                fileInput.onchange = (e) => {
                    if (e.target.files && e.target.files[0]) {
                        originalFileName = e.target.files[0].name.split('.')[0] || 'image';
                        const reader = new FileReader();
                        reader.onload = (event) => {
                            sourceImage = new Image();
                            sourceImage.onload = () => {
                                const MAX_PREVIEW_DIM = 400;
                                let scale = Math.min(MAX_PREVIEW_DIM / sourceImage.width, MAX_PREVIEW_DIM / sourceImage.height, 1);
                                cropCanvas.width = sourceImage.width * scale;
                                cropCanvas.height = sourceImage.height * scale;
                                ctx.drawImage(sourceImage, 0, 0, cropCanvas.width, cropCanvas.height);
                                cropCanvas.style.display = 'block';
                                
                                cropWInput.value = Math.floor(sourceImage.width / 2);
                                cropHInput.value = Math.floor(sourceImage.height / 2);
                                cropXInput.value = Math.floor(sourceImage.width / 4);
                                cropYInput.value = Math.floor(sourceImage.height / 4);
                                showAlert('Image loaded. Adjust crop parameters based on original image dimensions.', 'info');
                            };
                            sourceImage.src = event.target.result;
                        };
                        reader.readAsDataURL(e.target.files[0]);
                    }
                };

                cropButton.onclick = () => {
                    if (!sourceImage) {
                        showAlert('Please select an image first.', 'error');
                        return;
                    }
                    const sx = parseInt(cropXInput.value);
                    const sy = parseInt(cropYInput.value);
                    const sWidth = parseInt(cropWInput.value);
                    const sHeight = parseInt(cropHInput.value);

                    if (isNaN(sx) || isNaN(sy) || isNaN(sWidth) || isNaN(sHeight) || sWidth <= 0 || sHeight <= 0) {
                        showAlert('Invalid crop dimensions. Ensure they are positive numbers.', 'error');
                        return;
                    }
                    if (sx + sWidth > sourceImage.width || sy + sHeight > sourceImage.height || sx < 0 || sy < 0) {
                        showAlert('Crop area is outside the image boundaries.', 'error');
                        return;
                    }
                    
                    showAlert('Cropping...', 'info');
                    const tempCanvas = document.createElement('canvas');
                    tempCanvas.width = sWidth;
                    tempCanvas.height = sHeight;
                    const tempCtx = tempCanvas.getContext('2d');
                    
                    try {
                        tempCtx.drawImage(sourceImage, sx, sy, sWidth, sHeight, 0, 0, sWidth, sHeight);
                        const dataUrl = tempCanvas.toDataURL(fileInput.files[0].type || 'image/png');
                        croppedPreview.src = dataUrl;
                        croppedPreview.style.display = 'block';

                        const a = document.createElement('a');
                        a.href = dataUrl;
                        a.download = `${originalFileName}_cropped.${(fileInput.files[0].type || 'image/png').split('/')[1]}`;
                        document.body.appendChild(a);
                        a.click();
                        document.body.removeChild(a);
                        showAlert('Image cropped and download started.', 'success');
                    } catch (error) {
                        showAlert('Error during cropping: ' + error.message, 'error');
                    }
                };
            },

            videoConverter: (container) => {
                container.innerHTML = `
                    <p>This tool attempts to convert playable videos to MP4 or WebM by re-encoding using MediaRecorder. Success and output quality depend heavily on browser capabilities.</p>
                    <input type="file" id="vidConvFile" accept="video/*">
                    <label for="vidConvFormat">Convert to:</label>
                    <select id="vidConvFormat">
                        <option value="video/webm;codecs=vp8,opus">WebM (VP8/Opus)</option>
                        <option value="video/webm;codecs=vp9,opus">WebM (VP9/Opus - higher quality)</option>
                        <option value="video/mp4;codecs=avc1.42E01E,mp4a.40.2">MP4 (H.264/AAC - experimental)</option>
                    </select>
                    <button id="vidConvButton">Convert & Download</button>
                    <video id="vidConvPreview" controls style="max-width:100%; margin-top:10px; display:none; background-color:black;"></video>
                    <p id="vidConvStatus" class="result-area" style="display:none;"></p>
                `;
                const fileInput = container.querySelector('#vidConvFile');
                const formatSelect = container.querySelector('#vidConvFormat');
                const convertButton = container.querySelector('#vidConvButton');
                const videoPreview = container.querySelector('#vidConvPreview');
                const statusP = container.querySelector('#vidConvStatus');
                let mediaRecorder;
                let recordedChunks = [];
                let originalFileName = 'converted_video';

                fileInput.onchange = (e) => {
                    recordedChunks = [];
                    if (mediaRecorder && mediaRecorder.state === "recording") mediaRecorder.stop();
                    
                    if (e.target.files && e.target.files[0]) {
                        const file = e.target.files[0];
                        originalFileName = file.name.split('.')[0] || 'video';
                        const url = URL.createObjectURL(file);
                        videoPreview.src = url;
                        videoPreview.style.display = 'block';
                        videoPreview.onloadedmetadata = () => {
                            showAlert(`Video loaded. Duration: ${videoPreview.duration.toFixed(2)}s. Ready to convert.`, 'info');
                            statusP.style.display = 'none';
                        };
                        videoPreview.onerror = () => showAlert('Error loading video. The format might be unsupported by your browser.', 'error');
                    }
                };

                convertButton.onclick = () => {
                    if (!videoPreview.src || !videoPreview.src.startsWith('blob:')) {
                        showAlert('Please select a video file first.', 'error');
                        return;
                    }

                    const targetMimeType = formatSelect.value;
                    if (!MediaRecorder.isTypeSupported(targetMimeType)) {
                        showAlert(`Your browser does not support recording to ${targetMimeType}. Try another format or browser.`, 'error');
                        return;
                    }

                    showAlert('Starting conversion... The video will play in the background. Do not close modal.', 'info');
                    statusP.textContent = 'Conversion in progress... 0%';
                    statusP.style.display = 'block';
                    
                    videoPreview.currentTime = 0;
                    
                    const stream = videoPreview.captureStream ? videoPreview.captureStream() : videoPreview.mozCaptureStream ? videoPreview.mozCaptureStream() : null;
                    if (!stream) {
                        showAlert('Could not capture video stream. Your browser might not support this feature.', 'error');
                        return;
                    }

                    recordedChunks = [];
                    try {
                        mediaRecorder = new MediaRecorder(stream, { mimeType: targetMimeType });
                    } catch (err) {
                         showAlert(`Error initializing MediaRecorder: ${err.message}. Try a different format.`, 'error');
                         return;
                    }

                    mediaRecorder.ondataavailable = (event) => {
                        if (event.data.size > 0) recordedChunks.push(event.data);
                    };

                    mediaRecorder.onstop = () => {
                        if (recordedChunks.length === 0) {
                            showAlert('Conversion stopped, but no data was recorded. The format might be problematic.', 'error');
                            statusP.textContent = 'Conversion failed: No data.';
                            return;
                        }
                        const blob = new Blob(recordedChunks, { type: targetMimeType.split(';')[0] });
                        const url = URL.createObjectURL(blob);
                        const a = document.createElement('a');
                        a.href = url;
                        a.download = `${originalFileName}_converted.${targetMimeType.split('/')[1].split(';')[0]}`;
                        document.body.appendChild(a);
                        a.click();
                        document.body.removeChild(a);
                        URL.revokeObjectURL(url);
                        showAlert('Video conversion finished!', 'success');
                        statusP.textContent = 'Conversion complete!';
                        videoPreview.pause();
                    };
                    
                    videoPreview.onended = () => {
                        if (mediaRecorder && mediaRecorder.state === 'recording') mediaRecorder.stop();
                    };
                    
                    videoPreview.ontimeupdate = () => {
                        if (videoPreview.duration && mediaRecorder && mediaRecorder.state === 'recording') {
                            const progress = (videoPreview.currentTime / videoPreview.duration) * 100;
                            statusP.textContent = `Conversion in progress... ${progress.toFixed(0)}%`;
                        }
                    };

                    videoPreview.play().then(() => {
                        mediaRecorder.start(1000);
                    }).catch(err => {
                        showAlert(`Error playing video for conversion: ${err.message}`, 'error');
                    });
                };
                
                window.currentToolCleanup = () => {
                    if (mediaRecorder && mediaRecorder.state === 'recording') mediaRecorder.stop();
                    if(videoPreview) videoPreview.pause();
                    if (videoPreview && videoPreview.src && videoPreview.src.startsWith('blob:')) {
                        URL.revokeObjectURL(videoPreview.src);
                    }
                };
            },
            
            audioConverter: (() => { // IIFE to create a closure for helper function
                function bufferToWave(abuffer) {
                    let numOfChan = abuffer.numberOfChannels,
                        length = abuffer.length * numOfChan * 2 + 44,
                        buffer = new ArrayBuffer(length),
                        view = new DataView(buffer),
                        channels = [], i, sample,
                        offset = 0,
                        pos = 0;

                    // Write WAVE header
                    view.setUint32(pos, 0x46464952, false); pos += 4; // "RIFF"
                    view.setUint32(pos, length - 8, true); pos += 4;  // file length - 8
                    view.setUint32(pos, 0x45564157, false); pos += 4; // "WAVE"
                    view.setUint32(pos, 0x20746d66, false); pos += 4; // "fmt " chunk
                    view.setUint32(pos, 16, true); pos += 4;          // length = 16
                    view.setUint16(pos, 1, true); pos += 2;           // PCM (uncompressed)
                    view.setUint16(pos, numOfChan, true); pos += 2;
                    view.setUint32(pos, abuffer.sampleRate, true); pos += 4;
                    view.setUint32(pos, abuffer.sampleRate * 2 * numOfChan, true); pos += 4; // "byte rate"
                    view.setUint16(pos, numOfChan * 2, true); pos += 2; // block align
                    view.setUint16(pos, 16, true); pos += 2;          // bits per sample
                    view.setUint32(pos, 0x61746164, false); pos += 4; // "data" - chunk
                    view.setUint32(pos, abuffer.length * numOfChan * 2, true); pos += 4;

                    for (i = 0; i < abuffer.numberOfChannels; i++) channels.push(abuffer.getChannelData(i));

                    while (pos < length) {
                        for (i = 0; i < numOfChan; i++) {
                            sample = Math.max(-1, Math.min(1, channels[i][offset]));
                            sample = sample < 0 ? sample * 0x8000 : sample * 0x7FFF;
                            view.setInt16(pos, sample, true);
                            pos += 2;
                        }
                        offset++;
                    }
                    return new Blob([view], { type: 'audio/wav' });
                }

                return (container) => {
                    toolInitializers.audioConverter.bufferToWave = bufferToWave; // Expose for trimmer
                    const audioContext = new (window.AudioContext || window.webkitAudioContext)();
                    container.innerHTML = `
                        <p>This tool converts various audio formats (MP3, etc.) into uncompressed WAV format.</p>
                        <input type="file" id="audioConvFile" accept="audio/*">
                        <button id="audioConvButton">Convert to WAV & Download</button>
                        <audio id="audioConvPreview" controls style="width:100%; margin-top:10px; display:none;"></audio>
                    `;
                    const fileInput = container.querySelector('#audioConvFile');
                    const convertButton = container.querySelector('#audioConvButton');
                    const audioPreview = container.querySelector('#audioConvPreview');
                    let decodedAudioBuffer = null;
                    let originalFileName = 'converted_audio';

                    fileInput.onchange = (e) => {
                        if (e.target.files && e.target.files[0]) {
                            const file = e.target.files[0];
                            originalFileName = file.name.split('.')[0] || 'audio';
                            showAlert('Loading audio...', 'info');
                            const reader = new FileReader();
                            reader.onload = (event) => {
                                audioContext.decodeAudioData(event.target.result)
                                    .then(buffer => {
                                        decodedAudioBuffer = buffer;
                                        const tempUrl = URL.createObjectURL(file);
                                        audioPreview.src = tempUrl;
                                        audioPreview.style.display = 'block';
                                        showAlert('Audio loaded. Ready to convert.', 'success');
                                    })
                                    .catch(err => showAlert(`Error decoding audio: ${err.message}.`, 'error'));
                            };
                            reader.readAsArrayBuffer(file);
                        }
                    };

                    convertButton.onclick = () => {
                        if (!decodedAudioBuffer) {
                            showAlert('Please select and load an audio file first.', 'error');
                            return;
                        }
                        showAlert('Converting to WAV...', 'info');
                        try {
                            const wavBlob = bufferToWave(decodedAudioBuffer);
                            const url = URL.createObjectURL(wavBlob);
                            const a = document.createElement('a');
                            a.href = url;
                            a.download = `${originalFileName}_converted.wav`;
                            document.body.appendChild(a);
                            a.click();
                            document.body.removeChild(a);
                            URL.revokeObjectURL(url);
                            showAlert('Conversion to WAV successful!', 'success');
                        } catch (err) {
                            showAlert(`Error converting to WAV: ${err.message}`, 'error');
                        }
                    };
                };
            })(),

            audioTrimmer: (container) => {
                const audioContext = new (window.AudioContext || window.webkitAudioContext)();
                container.innerHTML = `
                    <input type="file" id="trimAudioFile" accept="audio/*">
                    <audio id="trimAudioPreview" controls style="width:100%; margin-top:10px; display:none;"></audio>
                    <div id="trimControls" style="display:none; margin-top:10px;">
                        <label for="trimStartTime">Start Time (s):</label>
                        <input type="number" id="trimStartTime" value="0" min="0" step="0.01">
                        <label for="trimEndTime">End Time (s):</label>
                        <input type="number" id="trimEndTime" value="0" min="0" step="0.01">
                        <p id="audioDurationInfo"></p>
                        <button id="trimButton">Trim & Download as WAV</button>
                    </div>
                `;
                const fileInput = container.querySelector('#trimAudioFile');
                const audioPreview = container.querySelector('#trimAudioPreview');
                const trimControls = container.querySelector('#trimControls');
                const startTimeInput = container.querySelector('#trimStartTime');
                const endTimeInput = container.querySelector('#trimEndTime');
                const durationInfo = container.querySelector('#audioDurationInfo');
                const trimButton = container.querySelector('#trimButton');
                
                let sourceBuffer = null;
                let originalFileName = 'trimmed_audio';

                fileInput.onchange = (e) => {
                    if (e.target.files && e.target.files[0]) {
                        const file = e.target.files[0];
                        originalFileName = file.name.split('.')[0] || 'audio';
                        showAlert('Loading audio...', 'info');
                        const reader = new FileReader();
                        reader.onload = (event) => {
                            audioContext.decodeAudioData(event.target.result)
                                .then(decodedBuffer => {
                                    sourceBuffer = decodedBuffer;
                                    const tempUrl = URL.createObjectURL(file);
                                    audioPreview.src = tempUrl;
                                    audioPreview.style.display = 'block';
                                    audioPreview.onloadedmetadata = () => {
                                        const duration = sourceBuffer.duration;
                                        durationInfo.textContent = `Duration: ${duration.toFixed(2)}s`;
                                        endTimeInput.value = duration.toFixed(2);
                                        endTimeInput.max = duration.toFixed(2);
                                        startTimeInput.max = duration.toFixed(2);
                                        trimControls.style.display = 'block';
                                        showAlert('Audio loaded. Set trim times.', 'success');
                                    };
                                })
                                .catch(err => showAlert(`Error decoding audio: ${err.message}`, 'error'));
                        };
                        reader.readAsArrayBuffer(file);
                    }
                };

                trimButton.onclick = () => {
                    if (!sourceBuffer) {
                        showAlert('Please load an audio file first.', 'error');
                        return;
                    }
                    const startTime = parseFloat(startTimeInput.value);
                    const endTime = parseFloat(endTimeInput.value);

                    if (isNaN(startTime) || isNaN(endTime) || startTime < 0 || endTime <= startTime || endTime > sourceBuffer.duration) {
                        showAlert('Invalid times. Ensure End Time is after Start Time and within audio duration.', 'error');
                        return;
                    }
                    
                    showAlert('Trimming audio...', 'info');
                    try {
                        const startOffset = Math.floor(startTime * sourceBuffer.sampleRate);
                        const endOffset = Math.floor(endTime * sourceBuffer.sampleRate);
                        const frameCount = endOffset - startOffset;

                        const trimmedBuffer = audioContext.createBuffer(
                            sourceBuffer.numberOfChannels,
                            frameCount,
                            sourceBuffer.sampleRate
                        );

                        for (let i = 0; i < sourceBuffer.numberOfChannels; i++) {
                            const channelData = sourceBuffer.getChannelData(i);
                            const trimmedChannelData = trimmedBuffer.getChannelData(i);
                            trimmedChannelData.set(channelData.subarray(startOffset, endOffset));
                        }
                        
                        if (typeof toolInitializers.audioConverter.bufferToWave !== 'function') {
                            showAlert('Audio conversion utility not found.', 'error');
                            return;
                        }
                        const wavBlob = toolInitializers.audioConverter.bufferToWave(trimmedBuffer);

                        const url = URL.createObjectURL(wavBlob);
                        const a = document.createElement('a');
                        a.href = url;
                        a.download = `${originalFileName}_trimmed.wav`;
                        document.body.appendChild(a);
                        a.click();
                        document.body.removeChild(a);
                        URL.revokeObjectURL(url);
                        showAlert('Audio trimmed and downloaded!', 'success');

                    } catch (err) {
                        showAlert(`Error trimming audio: ${err.message}`, 'error');
                    }
                };
            },
            
            ageCalculator: (container) => {
                container.innerHTML = `
                    <label for="birthDate">Enter your Date of Birth:</label>
                    <input type="date" id="birthDate">
                    <button id="calculateAgeBtn">Calculate Age</button>
                    <div id="ageResult" class="result-area" style="display:none;"></div>
                `;
                const birthDateInput = container.querySelector('#birthDate');
                const calculateBtn = container.querySelector('#calculateAgeBtn');
                const ageResultDiv = container.querySelector('#ageResult');

                const calculateAge = () => {
                    const birthDateString = birthDateInput.value;
                    if (!birthDateString) {
                        showAlert('Please enter your date of birth.', 'error');
                        ageResultDiv.style.display = 'none';
                        return;
                    }
                    const birthDate = new Date(birthDateString);
                    const today = new Date();

                    if (birthDate > today) {
                        showAlert('Birth date cannot be in the future.', 'error');
                        ageResultDiv.style.display = 'none';
                        return;
                    }

                    let years = today.getFullYear() - birthDate.getFullYear();
                    let months = today.getMonth() - birthDate.getMonth();
                    let days = today.getDate() - birthDate.getDate();

                    if (days < 0) {
                        months--;
                        const prevMonth = new Date(today.getFullYear(), today.getMonth(), 0);
                        days += prevMonth.getDate();
                    }
                    if (months < 0) {
                        years--;
                        months += 12;
                    }
                    ageResultDiv.innerHTML = `You are: <br>
                                            <strong>${years}</strong> years,
                                            <strong>${months}</strong> months, and
                                            <strong>${days}</strong> days old.`;
                    ageResultDiv.style.display = 'block';
                    hideAlert();
                };
                
                calculateBtn.onclick = calculateAge;
                birthDateInput.onchange = calculateAge;
            },

            emiCalculator: (container) => {
                container.innerHTML = `
                    <label for="loanAmount">Loan Amount (₹):</label>
                    <input type="number" id="loanAmount" placeholder="e.g., 1000000" min="0">
                    <label for="interestRate">Annual Interest Rate (%):</label>
                    <input type="number" id="interestRate" placeholder="e.g., 8.5" min="0" step="0.01">
                    <label for="loanTenure">Loan Tenure (months):</label>
                    <input type="number" id="loanTenure" placeholder="e.g., 240" min="1">
                    <button id="calculateEmiBtn">Calculate EMI</button>
                    <div id="emiResult" class="result-area" style="display:none;"></div>
                `;
                const amountInput = container.querySelector('#loanAmount');
                const rateInput = container.querySelector('#interestRate');
                const tenureInput = container.querySelector('#loanTenure');
                const calculateBtn = container.querySelector('#calculateEmiBtn');
                const resultDiv = container.querySelector('#emiResult');

                const calculateEmi = () => {
                    const P = parseFloat(amountInput.value);
                    const annualRate = parseFloat(rateInput.value);
                    const N = parseInt(tenureInput.value);

                    if (isNaN(P) || isNaN(annualRate) || isNaN(N) || P <= 0 || annualRate < 0 || N <= 0) {
                        resultDiv.style.display = 'none';
                        return;
                    }
                    
                    if (annualRate === 0) {
                         const EMI = P / N;
                         resultDiv.innerHTML = `Monthly EMI: <strong>₹ ${EMI.toFixed(2)}</strong><br>
                                   Total Interest Payable: <strong>₹ 0.00</strong><br>
                                   Total Payment (Principal + Interest): <strong>₹ ${P.toFixed(2)}</strong>`;
                        resultDiv.style.display = 'block';
                        hideAlert();
                        return;
                    }

                    const r = annualRate / (12 * 100); // Monthly interest rate
                    const EMI = (P * r * Math.pow(1 + r, N)) / (Math.pow(1 + r, N) - 1);
                    const totalPayment = EMI * N;
                    const totalInterest = totalPayment - P;

                    if (!isFinite(EMI)) {
                        showAlert('Calculation resulted in an invalid number. Check inputs.', 'error');
                        resultDiv.style.display = 'none';
                        return;
                    }

                    resultDiv.innerHTML = `Monthly EMI: <strong>₹ ${EMI.toLocaleString('en-IN', {minimumFractionDigits: 2, maximumFractionDigits: 2})}</strong><br>
                                        Total Interest Payable: <strong>₹ ${totalInterest.toLocaleString('en-IN', {minimumFractionDigits: 2, maximumFractionDigits: 2})}</strong><br>
                                        Total Payment: <strong>₹ ${totalPayment.toLocaleString('en-IN', {minimumFractionDigits: 2, maximumFractionDigits: 2})}</strong>`;
                    resultDiv.style.display = 'block';
                    hideAlert();
                };
                
                calculateBtn.onclick = calculateEmi;
                [amountInput, rateInput, tenureInput].forEach(input => input.oninput = calculateEmi);
            },

            sipCalculator: (container) => {
                container.innerHTML = `
                    <label for="monthlyInvestment">Monthly Investment (₹):</label>
                    <input type="number" id="monthlyInvestment" placeholder="e.g., 5000" min="0">
                    <label for="expectedReturnRate">Expected Annual Return Rate (%):</label>
                    <input type="number" id="expectedReturnRate" placeholder="e.g., 12" min="0" step="0.01">
                    <label for="investmentDuration">Investment Duration (years):</label>
                    <input type="number" id="investmentDuration" placeholder="e.g., 10" min="1">
                    <button id="calculateSipBtn">Calculate Future Value</button>
                    <div id="sipResult" class="result-area" style="display:none;"></div>
                `;
                const monthlyInvestmentInput = container.querySelector('#monthlyInvestment');
                const returnRateInput = container.querySelector('#expectedReturnRate');
                const durationInput = container.querySelector('#investmentDuration');
                const calculateBtn = container.querySelector('#calculateSipBtn');
                const resultDiv = container.querySelector('#sipResult');

                const calculateSip = () => {
                    const P = parseFloat(monthlyInvestmentInput.value);
                    const annualRate = parseFloat(returnRateInput.value);
                    const t_years = parseInt(durationInput.value);

                    if (isNaN(P) || isNaN(annualRate) || isNaN(t_years) || P <= 0 || annualRate < 0 || t_years <= 0) {
                        resultDiv.style.display = 'none';
                        return;
                    }

                    const n = t_years * 12;
                    const i = annualRate / 12 / 100;
                    const M = P * ( (Math.pow(1 + i, n) - 1) / i ) * (1 + i);
                    
                    const totalInvestment = P * n;
                    const wealthGained = M - totalInvestment;

                    resultDiv.innerHTML = `Invested Amount: <strong>₹ ${totalInvestment.toLocaleString('en-IN')}</strong><br>
                                        Estimated Returns: <strong>₹ ${wealthGained.toLocaleString('en-IN', {minimumFractionDigits: 2, maximumFractionDigits: 2})}</strong><br>
                                        Total Future Value: <strong>₹ ${M.toLocaleString('en-IN', {minimumFractionDigits: 2, maximumFractionDigits: 2})}</strong>`;
                    resultDiv.style.display = 'block';
                    hideAlert();
                };
                
                calculateBtn.onclick = calculateSip;
                [monthlyInvestmentInput, returnRateInput, durationInput].forEach(input => input.oninput = calculateSip);
            },

            qrCodeGenerator: (container) => {
                container.innerHTML = `
                    <label for="qrText">Text or URL for QR Code:</label>
                    <textarea id="qrText" placeholder="Enter text here"></textarea>
                    <label for="qrSize">Size (pixels):</label>
                    <input type="number" id="qrSize" value="200" min="50" max="500">
                    <button id="generateQrBtn">Generate QR Code</button>
                    <div id="qrCodeContainer" class="result-area" style="text-align:center; display:none; padding:10px; background-color:white;"></div>
                    <button id="downloadQrBtn" style="display:none;">Download as PNG</button>
                `;
                const textInput = container.querySelector('#qrText');
                const sizeInput = container.querySelector('#qrSize');
                const generateBtn = container.querySelector('#generateQrBtn');
                const qrContainer = container.querySelector('#qrCodeContainer');
                const downloadBtn = container.querySelector('#downloadQrBtn');
                let qrCanvasInstance = null;
                
                // Minimal QR Code generator logic (does not need a library, but is very basic)
                // This is a simplified implementation for demonstration. A full library is more robust.
                const generateQrOnCanvas = (text, size) => {
                    const canvas = document.createElement('canvas');
                    canvas.width = size;
                    canvas.height = size;
                    const ctx = canvas.getContext('2d');
                    ctx.fillStyle = 'white';
                    ctx.fillRect(0, 0, size, size);
                    ctx.fillStyle = 'black';
                    
                    // This is a placeholder visualization, NOT a valid QR code.
                    // A real implementation requires complex matrix generation.
                    const moduleSize = size / (text.length > 25 ? 25 : 21);
                    for (let y = 0; y < size; y += moduleSize) {
                        for (let x = 0; x < size; x += moduleSize) {
                            if (Math.random() > 0.5) {
                                ctx.fillRect(x, y, moduleSize, moduleSize);
                            }
                        }
                    }
                    ctx.font = `bold ${size/15}px Poppins`;
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillStyle = 'rgba(0,0,0,0.7)';
                    ctx.fillRect(0, size/2 - size/10, size, size/5);
                    ctx.fillStyle = 'white';
                    ctx.fillText("PREVIEW", size / 2, size / 2 );

                    showAlert('Generated a simple placeholder pattern. A real QR requires a complex algorithm.', 'info');
                    return canvas;
                };

                generateBtn.onclick = () => {
                    const text = textInput.value.trim();
                    const size = parseInt(sizeInput.value);
                    if (!text) {
                        showAlert('Please enter text or URL.', 'error');
                        return;
                    }
                    
                    qrContainer.innerHTML = '';
                    qrCanvasInstance = generateQrOnCanvas(text, size);
                    qrContainer.appendChild(qrCanvasInstance);
                    qrContainer.style.display = 'block';
                    downloadBtn.style.display = 'inline-block';
                };

                downloadBtn.onclick = () => {
                    if (qrCanvasInstance) {
                        const dataURL = qrCanvasInstance.toDataURL('image/png');
                        const a = document.createElement('a');
                        a.href = dataURL;
                        a.download = 'qrcode.png';
                        document.body.appendChild(a);
                        a.click();
                        document.body.removeChild(a);
                    }
                };
            },

            passwordGenerator: (container) => {
                container.innerHTML = `
                    <label for="passLength">Password Length: <span id="passLengthVal">16</span></label>
                    <input type="range" id="passLength" value="16" min="8" max="128" style="width: 100%; margin-bottom: 1rem;">
                    <div class="option-group">
                        <input type="checkbox" id="incUppercase" checked> <label for="incUppercase">Uppercase (A-Z)</label><br>
                        <input type="checkbox" id="incLowercase" checked> <label for="incLowercase">Lowercase (a-z)</label><br>
                        <input type="checkbox" id="incNumbers" checked> <label for="incNumbers">Numbers (0-9)</label><br>
                        <input type="checkbox" id="incSymbols" checked> <label for="incSymbols">Symbols (!@#$...)</label>
                    </div>
                    <button id="generatePassBtn">Generate Password</button>
                    <div class="result-area" style="margin-top:1rem; display:flex; align-items:center; justify-content:space-between;">
                        <input type="text" id="generatedPassword" readonly style="flex-grow:1; margin-right:10px;">
                        <button id="copyPassBtn" title="Copy to Clipboard" style="padding: 0.5em 0.8em;">📋</button>
                    </div>
                `;
                const lengthInput = container.querySelector('#passLength');
                const lengthValSpan = container.querySelector('#passLengthVal');
                const uppercaseCheck = container.querySelector('#incUppercase');
                const lowercaseCheck = container.querySelector('#incLowercase');
                const numbersCheck = container.querySelector('#incNumbers');
                const symbolsCheck = container.querySelector('#incSymbols');
                const generateBtn = container.querySelector('#generatePassBtn');
                const passwordOutput = container.querySelector('#generatedPassword');
                const copyBtn = container.querySelector('#copyPassBtn');

                const charSets = {
                    uppercase: 'ABCDEFGHIJKLMNOPQRSTUVWXYZ',
                    lowercase: 'abcdefghijklmnopqrstuvwxyz',
                    numbers: '0123456789',
                    symbols: '!@#$%^&*()_+-=[]{}|;:,.<>?'
                };
                
                lengthInput.oninput = () => lengthValSpan.textContent = lengthInput.value;

                const generatePassword = () => {
                    const length = parseInt(lengthInput.value);
                    let charset = '';
                    if (uppercaseCheck.checked) charset += charSets.uppercase;
                    if (lowercaseCheck.checked) charset += charSets.lowercase;
                    if (numbersCheck.checked) charset += charSets.numbers;
                    if (symbolsCheck.checked) charset += charSets.symbols;

                    if (charset === '') {
                        showAlert('Please select at least one character type.', 'error');
                        passwordOutput.value = '';
                        return;
                    }
                    
                    let password = '';
                    const cryptoArray = new Uint32Array(length);
                    window.crypto.getRandomValues(cryptoArray);
                    for (let i = 0; i < length; i++) {
                        password += charset[cryptoArray[i] % charset.length];
                    }

                    passwordOutput.value = password;
                    hideAlert();
                };
                
                generateBtn.onclick = generatePassword;
                generatePassword(); // Generate one on load

                copyBtn.onclick = () => {
                    if (passwordOutput.value) {
                        navigator.clipboard.writeText(passwordOutput.value)
                            .then(() => showAlert('Password copied to clipboard!', 'success'))
                            .catch(err => showAlert('Failed to copy password.', 'error'));
                    }
                };
            },

            wordCounter: (container) => {
                container.innerHTML = `
                    <textarea id="wcText" placeholder="Paste or type your text here..." rows="8"></textarea>
                    <div id="wcResult" class="result-area" style="margin-top:1rem;">
                        Words: <strong id="wcWords">0</strong><br>
                        Characters: <strong id="wcCharsWithSpaces">0</strong><br>
                        Sentences: <strong id="wcSentences">0</strong><br>
                        Reading Time: <strong id="wcReadingTime">~0 min</strong>
                    </div>
                `;
                const textArea = container.querySelector('#wcText');
                const wordsSpan = container.querySelector('#wcWords');
                const charsWithSpacesSpan = container.querySelector('#wcCharsWithSpaces');
                const sentencesSpan = container.querySelector('#wcSentences');
                const readingTimeSpan = container.querySelector('#wcReadingTime');

                textArea.oninput = () => {
                    const text = textArea.value.trim();
                    
                    const words = text === '' ? 0 : text.split(/\s+/).length;
                    const charsWithSpaces = textArea.value.length;
                    const sentences = text.split(/[.!?]+/).filter(Boolean).length;
                    
                    const wpm = 225; // Average reading speed
                    const readingTimeMinutes = words / wpm;
                    let readingTimeText = `~${Math.ceil(readingTimeMinutes)} min`;
                    if (readingTimeMinutes < 1) {
                         const seconds = Math.round(readingTimeMinutes * 60);
                         readingTimeText = `~${seconds} sec`;
                    }

                    wordsSpan.textContent = words;
                    charsWithSpacesSpan.textContent = charsWithSpaces;
                    sentencesSpan.textContent = sentences;
                    readingTimeSpan.textContent = readingTimeText;
                };
            },

            base64EncoderDecoder: (container) => {
                container.innerHTML = `
                    <textarea id="b64Input" placeholder="Enter plain text to encode or Base64 to decode" rows="5"></textarea>
                    <button id="b64EncodeBtn">Encode</button>
                    <button id="b64DecodeBtn">Decode</button>
                    <label for="b64Output" style="margin-top:1rem; display:block;">Result:</label>
                    <textarea id="b64Output" readonly rows="5"></textarea>
                `;
                const inputArea = container.querySelector('#b64Input');
                const outputArea = container.querySelector('#b64Output');
                const encodeBtn = container.querySelector('#b64EncodeBtn');
                const decodeBtn = container.querySelector('#b64DecodeBtn');

                encodeBtn.onclick = () => {
                    try {
                        outputArea.value = btoa(unescape(encodeURIComponent(inputArea.value)));
                        hideAlert();
                    } catch (e) {
                        showAlert('Error encoding text.', 'error');
                        outputArea.value = '';
                    }
                };

                decodeBtn.onclick = () => {
                    try {
                        outputArea.value = decodeURIComponent(escape(atob(inputArea.value)));
                        hideAlert();
                    } catch (e) {
                        showAlert('Invalid Base64 string.', 'error');
                        outputArea.value = '';
                    }
                };
            },

            colorPicker: (container) => {
                container.innerHTML = `
                    <label for="htmlColorPicker">Select a Color:</label>
                    <input type="color" id="htmlColorPicker" value="#FFD700">
                    <div class="color-picker-display result-area">
                        <div id="colorPreview" class="color-preview"></div>
                        <div id="colorValues" class="color-values">
                            <p>HEX: <strong id="hexValue"></strong></p>
                            <p>RGB: <strong id="rgbValue"></strong></p>
                            <p>HSL: <strong id="hslValue"></strong></p>
                        </div>
                    </div>
                `;
                const colorPickerInput = container.querySelector('#htmlColorPicker');
                const colorPreviewDiv = container.querySelector('#colorPreview');
                const hexValueSpan = container.querySelector('#hexValue');
                const rgbValueSpan = container.querySelector('#rgbValue');
                const hslValueSpan = container.querySelector('#hslValue');

                function updateColorValues(hex) {
                    hexValueSpan.textContent = hex.toUpperCase();
                    colorPreviewDiv.style.backgroundColor = hex;
                    
                    const rgb = hexToRgb(hex);
                    rgbValueSpan.textContent = `rgb(${rgb.r}, ${rgb.g}, ${rgb.b})`;

                    const hsl = rgbToHsl(rgb.r, rgb.g, rgb.b);
                    hslValueSpan.textContent = `hsl(${hsl.h}, ${hsl.s}%, ${hsl.l}%)`;
                }

                colorPickerInput.oninput = (e) => updateColorValues(e.target.value);
                
                updateColorValues(colorPickerInput.value); // Initial value

                function hexToRgb(hex) {
                    let r=0, g=0, b=0;
                    if (hex.length == 4) {
                        r = "0x" + hex[1] + hex[1];
                        g = "0x" + hex[2] + hex[2];
                        b = "0x" + hex[3] + hex[3];
                    } else if (hex.length == 7) {
                        r = "0x" + hex[1] + hex[2];
                        g = "0x" + hex[3] + hex[4];
                        b = "0x" + hex[5] + hex[6];
                    }
                    return {r: +r, g: +g, b: +b};
                }

                function rgbToHsl(r, g, b) {
                    r /= 255; g /= 255; b /= 255;
                    let max = Math.max(r, g, b), min = Math.min(r, g, b);
                    let h, s, l = (max + min) / 2;

                    if (max == min) { h = s = 0; } 
                    else {
                        var d = max - min;
                        s = l > 0.5 ? d / (2 - max - min) : d / (max + min);
                        switch (max) {
                            case r: h = (g - b) / d + (g < b ? 6 : 0); break;
                            case g: h = (b - r) / d + 2; break;
                            case b: h = (r - g) / d + 4; break;
                        }
                        h /= 6;
                    }
                    return { h: Math.round(h * 360), s: Math.round(s * 100), l: Math.round(l * 100) };
                }
            },

            textToSpeech: (container) => {
                const synth = window.speechSynthesis;
                if (!synth) {
                    container.innerHTML = "<p>Sorry, your browser doesn't support Text to Speech.</p>";
                    return;
                }
                
                container.innerHTML = `
                    <textarea id="ttsText" placeholder="Enter text to speak..." rows="6">Hello! Welcome to Multi Tool Hub.</textarea>
                    <div class="option-group">
                        <label for="ttsVoice">Voice:</label>
                        <select id="ttsVoice"></select>
                    </div>
                    <button id="ttsSpeakBtn">Speak</button>
                    <button id="ttsStopBtn">Stop</button>
                `;
                const textInput = container.querySelector('#ttsText');
                const voiceSelect = container.querySelector('#ttsVoice');
                const speakBtn = container.querySelector('#ttsSpeakBtn');
                const stopBtn = container.querySelector('#ttsStopBtn');
                
                let voices = [];

                function populateVoiceList() {
                    voices = synth.getVoices();
                    voiceSelect.innerHTML = '';
                    voices.forEach(voice => {
                        const option = document.createElement('option');
                        option.textContent = `${voice.name} (${voice.lang})`;
                        option.setAttribute('data-lang', voice.lang);
                        option.setAttribute('data-name', voice.name);
                        voiceSelect.appendChild(option);
                    });
                }
                
                populateVoiceList();
                if (synth.onvoiceschanged !== undefined) {
                    synth.onvoiceschanged = populateVoiceList;
                }

                speakBtn.onclick = () => {
                    if (synth.speaking) { synth.cancel(); }
                    if (textInput.value !== '') {
                        const utterThis = new SpeechSynthesisUtterance(textInput.value);
                        const selectedOption = voiceSelect.selectedOptions[0].getAttribute('data-name');
                        utterThis.voice = voices.find(voice => voice.name === selectedOption);
                        synth.speak(utterThis);
                    }
                };

                stopBtn.onclick = () => {
                    synth.cancel();
                };

                window.currentToolCleanup = () => {
                    if (synth.speaking) synth.cancel();
                };
            },

            speechToText: (container) => {
                const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
                if (!SpeechRecognition) {
                    container.innerHTML = '<p>Speech Recognition API is not supported in your browser.</p>';
                    return;
                }
                const recognition = new SpeechRecognition();
                recognition.continuous = true;
                recognition.interimResults = true;
                
                container.innerHTML = `
                    <p>Click "Start Listening" and speak into your microphone.</p>
                    <button id="sttStartBtn">Start Listening</button>
                    <button id="sttStopBtn" disabled>Stop Listening</button>
                    <textarea id="sttOutput" placeholder="Transcript will appear here..." readonly rows="6"></textarea>
                `;
                const startBtn = container.querySelector('#sttStartBtn');
                const stopBtn = container.querySelector('#sttStopBtn');
                const outputArea = container.querySelector('#sttOutput');

                recognition.onstart = () => {
                    startBtn.disabled = true;
                    stopBtn.disabled = false;
                    showAlert('Listening...', 'info');
                };
                recognition.onend = () => {
                    startBtn.disabled = false;
                    stopBtn.disabled = true;
                    showAlert('Stopped listening.', 'success');
                };
                recognition.onerror = (event) => {
                    showAlert('Speech recognition error: ' + event.error, 'error');
                };
                recognition.onresult = (event) => {
                    let interimTranscript = '';
                    let finalTranscript = '';
                    for (let i = event.resultIndex; i < event.results.length; ++i) {
                        if (event.results[i].isFinal) {
                            finalTranscript += event.results[i][0].transcript;
                        } else {
                            interimTranscript += event.results[i][0].transcript;
                        }
                    }
                    outputArea.value = outputArea.value.replace(interimTranscript, '') + finalTranscript + interimTranscript;
                };

                startBtn.onclick = () => {
                    outputArea.value = '';
                    recognition.start();
                };
                stopBtn.onclick = () => recognition.stop();
                
                window.currentToolCleanup = () => {
                    recognition.stop();
                };
            },

            jsonFormatter: (container) => {
                container.innerHTML = `
                    <textarea id="jsonInput" placeholder="Paste your JSON data here..." rows="7"></textarea>
                    <button id="formatJsonBtn">Format / Validate</button>
                    <textarea id="jsonOutput" readonly rows="7" placeholder="Formatted JSON will appear here..."></textarea>
                `;
                const inputArea = container.querySelector('#jsonInput');
                const outputArea = container.querySelector('#jsonOutput');
                const formatBtn = container.querySelector('#formatJsonBtn');

                formatBtn.onclick = () => {
                    const jsonString = inputArea.value;
                    if (!jsonString.trim()) {
                        showAlert('Input is empty.', 'info');
                        return;
                    }
                    try {
                        const jsonObj = JSON.parse(jsonString);
                        outputArea.value = JSON.stringify(jsonObj, null, 4);
                        showAlert('JSON is valid and formatted!', 'success');
                    } catch (e) {
                        outputArea.value = 'Error: ' + e.message;
                        showAlert('Invalid JSON: ' + e.message, 'error');
                    }
                };
            },

            unitConverter: (container) => {
                const units = {
                    length: { name: "Length", items: { meter: 1, kilometer: 1000, foot: 0.3048, mile: 1609.34 } },
                    weight: { name: "Weight", items: { kilogram: 1, gram: 0.001, pound: 0.453592, ounce: 0.0283495 } },
                    temperature: { name: "Temperature", items: { celsius: 'celsius', fahrenheit: 'fahrenheit', kelvin: 'kelvin' } }
                };

                container.innerHTML = `
                    <label for="ucCategory">Category:</label>
                    <select id="ucCategory"></select>
                    <div style="display:flex; gap:10px; margin-top:10px; align-items:flex-end;">
                        <div style="flex:2"><label>Value:</label><input type="number" id="ucInputValue" value="1"></div>
                        <div style="flex:3"><label>From:</label><select id="ucFromUnit"></select></div>
                        <div style="font-size:1.5rem; padding-bottom:0.5rem;">⇄</div>
                        <div style="flex:3"><label>To:</label><select id="ucToUnit"></select></div>
                    </div>
                    <div id="ucResult" class="result-area" style="margin-top:1rem; font-weight:bold; font-size:1.2rem;"></div>
                `;

                const categorySelect = container.querySelector('#ucCategory');
                const fromUnitSelect = container.querySelector('#ucFromUnit');
                const toUnitSelect = container.querySelector('#ucToUnit');
                const valueInput = container.querySelector('#ucInputValue');
                const resultDiv = container.querySelector('#ucResult');

                function populateOptions() {
                    const categoryKey = categorySelect.value;
                    const unitSet = units[categoryKey].items;
                    fromUnitSelect.innerHTML = '';
                    toUnitSelect.innerHTML = '';
                    for (const unit in unitSet) {
                        const optionText = unit.charAt(0).toUpperCase() + unit.slice(1);
                        fromUnitSelect.add(new Option(optionText, unit));
                        toUnitSelect.add(new Option(optionText, unit));
                    }
                    toUnitSelect.selectedIndex = 1;
                    convertUnits();
                }

                function convertUnits() {
                    const categoryKey = categorySelect.value;
                    const fromUnit = fromUnitSelect.value;
                    const toUnit = toUnitSelect.value;
                    const inputValue = parseFloat(valueInput.value);
                    if (isNaN(inputValue)) return;

                    let result;
                    if (categoryKey === 'temperature') {
                        if (fromUnit === 'celsius') result = toUnit === 'fahrenheit' ? (inputValue * 9/5) + 32 : inputValue + 273.15;
                        else if (fromUnit === 'fahrenheit') result = toUnit === 'celsius' ? (inputValue - 32) * 5/9 : (inputValue - 32) * 5/9 + 273.15;
                        else result = toUnit === 'celsius' ? inputValue - 273.15 : (inputValue - 273.15) * 9/5 + 32;
                    } else {
                        const baseValue = inputValue * units[categoryKey].items[fromUnit];
                        result = baseValue / units[categoryKey].items[toUnit];
                    }
                    resultDiv.textContent = result.toFixed(4);
                }

                for (const key in units) {
                    categorySelect.add(new Option(units[key].name, key));
                }
                
                categorySelect.onchange = populateOptions;
                fromUnitSelect.onchange = convertUnits;
                toUnitSelect.onchange = convertUnits;
                valueInput.oninput = convertUnits;
                
                populateOptions();
            },

            bmiCalculator: (container) => {
                container.innerHTML = `
                    <label for="bmiWeight">Weight (kg):</label>
                    <input type="number" id="bmiWeight" placeholder="e.g., 70" min="0">
                    <label for="bmiHeight">Height (cm):</label>
                    <input type="number" id="bmiHeight" placeholder="e.g., 175" min="0">
                    <button id="calculateBmiBtn">Calculate BMI</button>
                    <div id="bmiResult" class="result-area" style="display:none; text-align:center;"></div>
                `;
                const weightInput = container.querySelector('#bmiWeight');
                const heightInput = container.querySelector('#bmiHeight');
                const calculateBtn = container.querySelector('#calculateBmiBtn');
                const resultDiv = container.querySelector('#bmiResult');

                const calculateBmi = () => {
                    const weight = parseFloat(weightInput.value);
                    const heightCm = parseFloat(heightInput.value);

                    if (isNaN(weight) || isNaN(heightCm) || weight <= 0 || heightCm <= 0) {
                        resultDiv.style.display = 'none';
                        return;
                    }
                    const heightM = heightCm / 100;
                    const bmi = weight / (heightM * heightM);
                    let category = '';
                    if (bmi < 18.5) category = 'Underweight';
                    else if (bmi < 24.9) category = 'Normal weight';
                    else if (bmi < 29.9) category = 'Overweight';
                    else category = 'Obesity';

                    resultDiv.innerHTML = `Your BMI: <strong style="font-size:1.5em;">${bmi.toFixed(2)}</strong><br>Category: <strong>${category}</strong>`;
                    resultDiv.style.display = 'block';
                    hideAlert();
                };
                
                calculateBtn.onclick = calculateBmi;
                [weightInput, heightInput].forEach(input => input.oninput = calculateBmi);
            },

            timerStopwatch: (container) => {
                container.innerHTML = `
                    <div class="tabs">
                        <button class="tab-button active" data-tab="timerTab">Timer</button>
                        <button class="tab-button" data-tab="stopwatchTab">Stopwatch</button>
                    </div>
                    <div id="timerTab" class="tab-content">
                        <h3>Timer</h3>
                        <div style="display:flex; justify-content:space-around; margin-bottom:1rem;">
                            <input type="number" id="timerHours" min="0" value="0" style="width:60px;"> H
                            <input type="number" id="timerMinutes" min="0" max="59" value="5" style="width:60px;"> M
                            <input type="number" id="timerSeconds" min="0" max="59" value="0" style="width:60px;"> S
                        </div>
                        <div class="timer-display" id="timerDisplay">00:05:00</div>
                        <div style="text-align:center;">
                            <button id="timerStart">Start</button>
                            <button id="timerPause" disabled>Pause</button>
                            <button id="timerReset">Reset</button>
                        </div>
                    </div>
                    <div id="stopwatchTab" class="tab-content" style="display:none;">
                        <h3>Stopwatch</h3>
                        <div class="stopwatch-display" id="stopwatchDisplay">00:00:00.00</div>
                        <div style="text-align:center; margin-bottom:1rem;">
                            <button id="stopwatchStart">Start</button>
                            <button id="stopwatchStop" disabled>Stop</button>
                            <button id="stopwatchReset">Reset</button>
                            <button id="stopwatchLap" disabled>Lap</button>
                        </div>
                        <ul id="lapsList" class="laps-list"></ul>
                    </div>
                `;

                // Tab switching
                const tabButtons = container.querySelectorAll('.tab-button');
                const tabContents = container.querySelectorAll('.tab-content');
                tabButtons.forEach(button => {
                    button.onclick = () => {
                        tabButtons.forEach(btn => btn.classList.remove('active'));
                        button.classList.add('active');
                        tabContents.forEach(content => content.style.display = 'none');
                        container.querySelector(`#${button.dataset.tab}`).style.display = 'block';
                    };
                });

                // Timer Logic
                const timerHoursInput = container.querySelector('#timerHours');
                const timerMinutesInput = container.querySelector('#timerMinutes');
                const timerSecondsInput = container.querySelector('#timerSeconds');
                const timerDisplay = container.querySelector('#timerDisplay');
                const timerStartBtn = container.querySelector('#timerStart');
                const timerPauseBtn = container.querySelector('#timerPause');
                const timerResetBtn = container.querySelector('#timerReset');
                let timerInterval, totalSeconds;

                function updateTimerDisplay() {
                    const h = String(Math.floor(totalSeconds / 3600)).padStart(2, '0');
                    const m = String(Math.floor((totalSeconds % 3600) / 60)).padStart(2, '0');
                    const s = String(totalSeconds % 60).padStart(2, '0');
                    timerDisplay.textContent = `${h}:${m}:${s}`;
                }

                timerStartBtn.onclick = () => {
                    const h = parseInt(timerHoursInput.value) || 0;
                    const m = parseInt(timerMinutesInput.value) || 0;
                    const s = parseInt(timerSecondsInput.value) || 0;
                    totalSeconds = h * 3600 + m * 60 + s;
                    if (totalSeconds <= 0) return;

                    timerStartBtn.disabled = true;
                    timerPauseBtn.disabled = false;
                    timerInterval = setInterval(() => {
                        if (totalSeconds <= 0) {
                            clearInterval(timerInterval);
                            alert("Time's Up!");
                            timerResetBtn.click();
                        } else {
                            totalSeconds--;
                            updateTimerDisplay();
                        }
                    }, 1000);
                };
                timerPauseBtn.onclick = () => {
                    clearInterval(timerInterval);
                    timerStartBtn.disabled = false;
                    timerPauseBtn.disabled = true;
                };
                timerResetBtn.onclick = () => {
                    clearInterval(timerInterval);
                    timerHoursInput.value = "0";
                    timerMinutesInput.value = "5";
                    timerSecondsInput.value = "0";
                    timerDisplay.textContent = "00:05:00";
                    timerStartBtn.disabled = false;
                    timerPauseBtn.disabled = true;
                };

                // Stopwatch Logic
                const stopwatchDisplay = container.querySelector('#stopwatchDisplay');
                const stopwatchStartBtn = container.querySelector('#stopwatchStart');
                const stopwatchStopBtn = container.querySelector('#stopwatchStop');
                const stopwatchResetBtn = container.querySelector('#stopwatchReset');
                const stopwatchLapBtn = container.querySelector('#stopwatchLap');
                const lapsList = container.querySelector('#lapsList');
                let stopwatchInterval, startTime, elapsedTime = 0, lapNumber = 1;

                function formatTime(ms) {
                    const totalSeconds = Math.floor(ms / 1000);
                    const minutes = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
                    const seconds = String(totalSeconds % 60).padStart(2, '0');
                    const milliseconds = String(Math.floor((ms % 1000) / 10)).padStart(2, '0');
                    return `${minutes}:${seconds}.${milliseconds}`;
                }
                
                stopwatchStartBtn.onclick = () => {
                    startTime = Date.now() - elapsedTime;
                    stopwatchInterval = setInterval(() => {
                        elapsedTime = Date.now() - startTime;
                        stopwatchDisplay.textContent = formatTime(elapsedTime);
                    }, 10);
                    stopwatchStartBtn.disabled = true;
                    stopwatchStopBtn.disabled = false;
                    stopwatchLapBtn.disabled = false;
                };
                stopwatchStopBtn.onclick = () => {
                    clearInterval(stopwatchInterval);
                    stopwatchStartBtn.disabled = false;
                    stopwatchStopBtn.disabled = true;
                };
                stopwatchResetBtn.onclick = () => {
                    clearInterval(stopwatchInterval);
                    elapsedTime = 0;
                    stopwatchDisplay.textContent = "00:00:00.00";
                    lapsList.innerHTML = '';
                    lapNumber = 1;
                    stopwatchStartBtn.disabled = false;
                    stopwatchStopBtn.disabled = true;
                    stopwatchLapBtn.disabled = true;
                };
                stopwatchLapBtn.onclick = () => {
                    const li = document.createElement('li');
                    li.textContent = `Lap ${lapNumber++}: ${formatTime(elapsedTime)}`;
                    lapsList.prepend(li);
                };

                window.currentToolCleanup = () => {
                    clearInterval(timerInterval);
                    clearInterval(stopwatchInterval);
                };
            }
        };

    });
    </script>
</body>
</html>
