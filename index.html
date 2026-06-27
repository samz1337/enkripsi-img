<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🔐 SecureImage - Enkripsi & Sensor Gambar</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0c0e1a 0%, #1a1f36 50%, #0c0e1a 100%);
            min-height: 100vh;
            padding: 2rem 1rem;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            position: relative;
        }

        /* Background animated particles */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(2px 2px at 20% 30%, rgba(99, 102, 241, 0.3), transparent),
                radial-gradient(2px 2px at 40% 70%, rgba(139, 92, 246, 0.2), transparent),
                radial-gradient(2px 2px at 60% 20%, rgba(99, 102, 241, 0.3), transparent),
                radial-gradient(2px 2px at 80% 80%, rgba(139, 92, 246, 0.2), transparent);
            background-size: 200px 200px;
            pointer-events: none;
            z-index: 0;
        }

        .container {
            position: relative;
            z-index: 1;
        }

        /* Glassmorphism Card */
        .card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 32px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.8), inset 0 1px 0 rgba(255, 255, 255, 0.05);
            color: #f1f5f9;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-2px);
            box-shadow: 0 30px 60px -12px rgba(0, 0, 0, 0.9), inset 0 1px 0 rgba(255, 255, 255, 0.08);
        }

        .card-header {
            background: rgba(255, 255, 255, 0.03);
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            font-weight: 700;
            padding: 1.5rem 2rem;
            font-size: 1.3rem;
            letter-spacing: 0.5px;
            border-radius: 32px 32px 0 0 !important;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .card-header .icon-wrapper {
            width: 40px;
            height: 40px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.2), rgba(139, 92, 246, 0.2));
        }

        .card-body {
            padding: 2rem;
        }

        /* Form Controls */
        .form-control {
            background: rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(255, 255, 255, 0.08);
            color: #f8fafc;
            border-radius: 16px;
            padding: 0.8rem 1.2rem;
            transition: all 0.3s ease;
            font-size: 0.95rem;
        }

        .form-control:focus {
            background: rgba(0, 0, 0, 0.6);
            border-color: #818cf8;
            box-shadow: 0 0 0 4px rgba(99, 102, 241, 0.15);
            color: #fff;
        }

        .form-control::placeholder {
            color: #64748b;
            opacity: 0.7;
        }

        .form-label {
            font-weight: 600;
            font-size: 0.9rem;
            letter-spacing: 0.3px;
            color: #cbd5e1;
            margin-bottom: 0.5rem;
        }

        /* Buttons */
        .btn {
            border-radius: 40px;
            padding: 0.7rem 2rem;
            font-weight: 600;
            transition: all 0.3s ease;
            letter-spacing: 0.3px;
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background: linear-gradient(135deg, #6366f1, #8b5cf6);
            border: none;
            box-shadow: 0 8px 24px -6px rgba(99, 102, 241, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-2px) scale(1.02);
            box-shadow: 0 12px 32px -6px rgba(99, 102, 241, 0.6);
        }

        .btn-primary:active {
            transform: scale(0.98);
        }

        .btn-success {
            background: linear-gradient(135deg, #10b981, #059669);
            border: none;
            box-shadow: 0 8px 24px -6px rgba(16, 185, 129, 0.4);
        }

        .btn-success:hover {
            transform: translateY(-2px) scale(1.02);
            box-shadow: 0 12px 32px -6px rgba(16, 185, 129, 0.6);
        }

        .btn-outline-light {
            border: 1px solid rgba(255, 255, 255, 0.15);
            color: #e2e8f0;
            background: rgba(255, 255, 255, 0.03);
        }

        .btn-outline-light:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }

        .btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none !important;
        }

        /* Image Preview */
        .image-preview {
            background: rgba(0, 0, 0, 0.4);
            border-radius: 20px;
            padding: 1.5rem;
            text-align: center;
            border: 2px dashed rgba(255, 255, 255, 0.06);
            min-height: 160px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            transition: all 0.3s ease;
            position: relative;
        }

        .image-preview.has-image {
            border-color: rgba(99, 102, 241, 0.3);
            background: rgba(99, 102, 241, 0.05);
        }

        .image-preview img {
            max-width: 100%;
            max-height: 250px;
            border-radius: 12px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
            transition: all 0.3s ease;
        }

        .image-preview .placeholder-icon {
            font-size: 3rem;
            color: #475569;
            opacity: 0.5;
            margin-bottom: 8px;
        }

        /* Sensor Effect - Blur & Pixelate */
        .sensor-overlay {
            position: relative;
            display: inline-block;
        }

        .sensor-overlay::before {
            content: '🔒';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 3rem;
            z-index: 2;
            text-shadow: 0 4px 20px rgba(0, 0, 0, 0.8);
            animation: pulse 2s ease-in-out infinite;
        }

        .sensor-overlay img {
            filter: blur(12px) brightness(0.7);
            transition: all 0.5s ease;
        }

        .sensor-overlay:hover img {
            filter: blur(8px) brightness(0.8);
        }

        @keyframes pulse {
            0%, 100% { transform: translate(-50%, -50%) scale(1); }
            50% { transform: translate(-50%, -50%) scale(1.1); }
        }

        /* Result Box */
        .result-box {
            background: rgba(0, 0, 0, 0.4);
            border-radius: 16px;
            padding: 1.2rem 1.5rem;
            word-break: break-all;
            font-size: 0.8rem;
            border-left: 4px solid #818cf8;
            max-height: 150px;
            overflow-y: auto;
            font-family: 'Courier New', monospace;
            color: #a5b4fc;
        }

        .result-box::-webkit-scrollbar {
            width: 4px;
        }

        .result-box::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
        }

        .result-box::-webkit-scrollbar-thumb {
            background: #818cf8;
            border-radius: 10px;
        }

        /* Badge */
        .badge-db {
            background: rgba(45, 55, 72, 0.8);
            color: #cbd5e1;
            padding: 0.4rem 1rem;
            border-radius: 40px;
            font-weight: 400;
            font-size: 0.75rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        /* Table */
        .table {
            color: #e2e8f0;
            font-size: 0.85rem;
            margin-bottom: 0;
        }

        .table th {
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            font-weight: 600;
            color: #94a3b8;
            text-transform: uppercase;
            font-size: 0.7rem;
            letter-spacing: 0.5px;
            padding: 0.8rem 0.5rem;
        }

        .table td {
            border-color: rgba(255, 255, 255, 0.04);
            vertical-align: middle;
            padding: 0.8rem 0.5rem;
        }

        .table tr {
            transition: background 0.2s ease;
        }

        .table tr:hover {
            background: rgba(255, 255, 255, 0.03);
        }

        .btn-sm-icon {
            background: rgba(255, 255, 255, 0.05);
            border: none;
            color: #a5b4fc;
            padding: 0.3rem 0.6rem;
            border-radius: 8px;
            transition: all 0.2s ease;
            margin: 0 2px;
        }

        .btn-sm-icon:hover {
            background: rgba(255, 255, 255, 0.1);
            color: #e0e7ff;
            transform: scale(1.1);
        }

        .btn-sm-icon.danger:hover {
            background: rgba(239, 68, 68, 0.2);
            color: #f87171;
        }

        /* Toast */
        .toast-container {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 9999;
            display: flex;
            flex-direction: column;
            gap: 10px;
            max-width: 400px;
        }

        .toast-custom {
            background: rgba(30, 41, 59, 0.95);
            backdrop-filter: blur(20px);
            color: #f1f5f9;
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 16px;
            padding: 1rem 1.5rem;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
            animation: slideInRight 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 0.9rem;
        }

        .toast-custom.success {
            border-left: 4px solid #10b981;
        }

        .toast-custom.error {
            border-left: 4px solid #ef4444;
        }

        @keyframes slideInRight {
            from {
                transform: translateX(120%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .toast-custom.removing {
            animation: slideOutRight 0.3s ease forwards;
        }

        @keyframes slideOutRight {
            to {
                transform: translateX(120%);
                opacity: 0;
            }
        }

        /* Loading Spinner */
        .loading-spinner {
            display: inline-block;
            width: 1.2rem;
            height: 1.2rem;
            border: 3px solid rgba(255, 255, 255, 0.15);
            border-radius: 50%;
            border-top-color: #fff;
            animation: spin 0.8s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Footer */
        .footer-info {
            color: #475569;
            font-size: 0.8rem;
            text-align: center;
            margin-top: 2.5rem;
            padding: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.03);
        }

        .footer-info i {
            color: #6366f1;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .card-body {
                padding: 1.25rem;
            }
            .card-header {
                padding: 1rem 1.25rem;
                font-size: 1.1rem;
            }
            .toast-container {
                top: 10px;
                right: 10px;
                max-width: 90%;
            }
        }

        /* Scrollbar Global */
        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.03);
        }

        ::-webkit-scrollbar-thumb {
            background: #475569;
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: #6366f1;
        }

        /* Glow effect on cards */
        .card.glow-primary {
            box-shadow: 0 0 40px rgba(99, 102, 241, 0.05), 0 25px 50px -12px rgba(0, 0, 0, 0.8);
        }

        .card.glow-success {
            box-shadow: 0 0 40px rgba(16, 185, 129, 0.05), 0 25px 50px -12px rgba(0, 0, 0, 0.8);
        }

        /* Sensor toggle switch */
        .sensor-toggle {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            padding: 8px 16px;
            border-radius: 40px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.08);
            transition: all 0.3s ease;
            user-select: none;
        }

        .sensor-toggle:hover {
            background: rgba(255, 255, 255, 0.08);
        }

        .sensor-toggle input {
            display: none;
        }

        .sensor-toggle .toggle-track {
            width: 44px;
            height: 24px;
            border-radius: 12px;
            background: #334155;
            transition: all 0.3s ease;
            position: relative;
        }

        .sensor-toggle .toggle-track::after {
            content: '';
            position: absolute;
            top: 2px;
            left: 2px;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #94a3b8;
            transition: all 0.3s ease;
        }

        .sensor-toggle input:checked + .toggle-track {
            background: #6366f1;
        }

        .sensor-toggle input:checked + .toggle-track::after {
            transform: translateX(20px);
            background: #fff;
        }

        .sensor-toggle .label-text {
            font-size: 0.85rem;
            color: #94a3b8;
        }

        .sensor-toggle .label-text.active {
            color: #818cf8;
        }
    </style>
</head>
<body>

<div class="toast-container" id="toastContainer"></div>

<div class="container">
    <div class="row justify-content-center">
        <div class="col-lg-10 col-xl-9">

            <!-- Header -->
            <div class="text-center mb-5">
                <div style="display: inline-flex; align-items: center; gap: 16px; background: rgba(255,255,255,0.03); padding: 0.5rem 2rem; border-radius: 60px; border: 1px solid rgba(255,255,255,0.05); backdrop-filter: blur(10px);">
                    <i class="fas fa-shield-halved text-primary" style="font-size: 2rem;"></i>
                    <h1 class="display-5 fw-bold text-white" style="text-shadow: 0 4px 30px rgba(0,0,0,0.5); letter-spacing: -0.5px;">
                        SecureImage
                    </h1>
                    <span class="badge" style="background: linear-gradient(135deg, #6366f1, #8b5cf6); padding: 0.3rem 1rem; border-radius: 40px; font-size: 0.7rem; letter-spacing: 0.5px; text-transform: uppercase;">AES-256</span>
                </div>
                <p class="text-secondary-custom mt-3" style="letter-spacing: 0.5px; opacity: 0.7;">
                    <i class="fas fa-lock me-2"></i>Enkripsi & Sensor Gambar · Database Lokal · Bisa Dibalik
                </p>
            </div>

            <!-- ENKRIPSI CARD -->
            <div class="card glow-primary mb-4">
                <div class="card-header">
                    <div class="icon-wrapper">
                        <i class="fas fa-cloud-upload-alt text-primary"></i>
                    </div>
                    <span>Unggah & Enkripsi Gambar</span>
                    <span class="badge-db ms-auto"><i class="far fa-clock me-1"></i> <span id="headerTime"></span></span>
                </div>
                <div class="card-body">
                    <form id="encryptForm">
                        <div class="row g-4">
                            <div class="col-md-5">
                                <label class="form-label"><i class="fas fa-image me-2"></i>Pilih Gambar</label>
                                <input class="form-control" type="file" id="imageInput" accept="image/*" required>
                                <div class="image-preview mt-3" id="previewContainer">
                                    <i class="fas fa-file-image placeholder-icon"></i>
                                    <span class="text-secondary-custom small">Belum ada gambar</span>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <label class="form-label"><i class="fas fa-key me-2"></i>Kunci Enkripsi</label>
                                <input type="text" class="form-control" id="secretKey" placeholder="Masukkan kunci" value="rahasia123">
                                <small class="text-secondary-custom d-block mt-2" style="font-size:0.75rem;">
                                    <i class="fas fa-info-circle me-1"></i>Gunakan kunci yang sama untuk dekripsi
                                </small>
                                <div class="mt-3">
                                    <label class="sensor-toggle">
                                        <span class="label-text"><i class="fas fa-eye-slash me-1"></i>Sensor</span>
                                        <input type="checkbox" id="sensorToggle" checked>
                                        <span class="toggle-track"></span>
                                        <span class="label-text active"><i class="fas fa-eye me-1"></i>Blur</span>
                                    </label>
                                </div>
                            </div>
                            <div class="col-md-3 d-grid gap-2">
                                <button type="submit" class="btn btn-primary btn-lg" id="encryptBtn">
                                    <i class="fas fa-lock me-2"></i>Enkripsi
                                </button>
                                <button type="button" class="btn btn-outline-light" id="clearFormBtn">
                                    <i class="fas fa-undo-alt me-1"></i>Reset
                                </button>
                            </div>
                        </div>
                    </form>

                    <!-- Hasil Enkripsi -->
                    <div id="encryptResultArea" class="mt-4" style="display: none;">
                        <hr class="border-secondary opacity-25">
                        <div class="row g-3">
                            <div class="col-md-7">
                                <div class="d-flex align-items-center gap-3 mb-2">
                                    <i class="fas fa-check-circle text-success fa-lg"></i>
                                    <h6 class="mb-0 fw-semibold">Hasil Enkripsi</h6>
                                    <span class="badge-db ms-2"><i class="far fa-clock me-1"></i> <span id="timestampEncrypt"></span></span>
                                </div>
                                <div class="result-box" id="encryptedResult">
                                    [data terenkripsi akan muncul di sini]
                                </div>
                                <button class="btn btn-outline-light btn-sm mt-2" id="copyEncryptedBtn">
                                    <i class="far fa-copy me-1"></i>Salin
                                </button>
                            </div>
                            <div class="col-md-5">
                                <div class="d-flex align-items-center gap-3 mb-2">
                                    <i class="fas fa-database text-warning fa-lg"></i>
                                    <h6 class="mb-0 fw-semibold">Database</h6>
                                    <span class="badge-db"><i class="fas fa-check-circle text-success me-1"></i> ID: <span id="recordIdDisplay">-</span></span>
                                </div>
                                <div class="p-3 rounded-3" style="background: rgba(0,0,0,0.2);">
                                    <div class="small text-secondary-custom">
                                        <i class="fas fa-info-circle me-1"></i> Data tersimpan di localStorage
                                    </div>
                                    <div class="small text-secondary-custom mt-1">
                                        <i class="fas fa-file me-1"></i> <span id="fileInfoDisplay">-</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- DEKRIPSI CARD -->
            <div class="card glow-success mb-4">
                <div class="card-header">
                    <div class="icon-wrapper" style="background: linear-gradient(135deg, rgba(16, 185, 129, 0.2), rgba(5, 150, 105, 0.2));">
                        <i class="fas fa-unlock-alt text-success"></i>
                    </div>
                    <span>Dekripsi & Sensor Gambar</span>
                </div>
                <div class="card-body">
                    <form id="decryptForm">
                        <div class="row g-3">
                            <div class="col-md-7">
                                <label class="form-label"><i class="fas fa-paste me-2"></i>Tempel Data Enkripsi</label>
                                <textarea class="form-control" id="decryptInput" rows="2" placeholder="Masukkan ciphertext dari hasil enkripsi..."></textarea>
                            </div>
                            <div class="col-md-3">
                                <label class="form-label"><i class="fas fa-key me-2"></i>Kunci</label>
                                <input type="text" class="form-control" id="decryptKey" placeholder="Kunci yang sama" value="rahasia123">
                            </div>
                            <div class="col-md-2 d-grid">
                                <button type="submit" class="btn btn-success btn-lg" id="decryptBtn">
                                    <i class="fas fa-undo me-2"></i>Balikkan
                                </button>
                            </div>
                        </div>
                    </form>

                    <!-- Hasil Dekripsi -->
                    <div id="decryptResultArea" class="mt-4" style="display: none;">
                        <hr class="border-secondary opacity-25">
                        <div class="row g-4">
                            <div class="col-md-6">
                                <h6 class="fw-semibold mb-3">
                                    <i class="fas fa-image text-info me-2"></i>Gambar Asli
                                    <span class="badge-db ms-2" id="sensorStatusBadge">
                                        <i class="fas fa-eye-slash me-1"></i>Sensor Aktif
                                    </span>
                                </h6>
                                <div class="image-preview has-image" id="decryptedPreviewContainer">
                                    <div class="sensor-overlay" id="sensorOverlay">
                                        <img id="decryptedImage" src="" alt="decrypted" style="max-height:250px; display:none;">
                                    </div>
                                    <div id="decryptedPlaceholder">
                                        <i class="fas fa-spinner fa-pulse text-secondary-custom"></i>
                                        <span class="text-secondary-custom small d-block mt-2">Menunggu dekripsi...</span>
                                    </div>
                                </div>
                            </div>
                            <div class="col-md-6">
                                <h6 class="fw-semibold mb-3">
                                    <i class="fas fa-info-circle text-info me-2"></i>Metadata
                                </h6>
                                <div class="result-box" id="decryptMeta" style="font-size:0.85rem; border-left-color: #10b981; min-height: 100px;">
                                    <span class="text-secondary-custom">Belum ada data</span>
                                </div>
                                <div class="d-flex gap-2 mt-3">
                                    <button class="btn btn-outline-light btn-sm" id="downloadDecryptedBtn">
                                        <i class="fas fa-download me-1"></i>Unduh
                                    </button>
                                    <button class="btn btn-outline-light btn-sm" id="toggleSensorBtn">
                                        <i class="fas fa-eye-slash me-1"></i>Toggle Sensor
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- DATABASE TABLE -->
            <div class="card">
                <div class="card-header">
                    <div class="icon-wrapper" style="background: linear-gradient(135deg, rgba(234, 179, 8, 0.2), rgba(234, 179, 8, 0.1));">
                        <i class="fas fa-table text-warning"></i>
                    </div>
                    <span>Riwayat Database</span>
                    <button class="btn btn-outline-light btn-sm ms-auto" id="refreshDbBtn">
                        <i class="fas fa-sync-alt me-1"></i>Segarkan
                    </button>
                    <button class="btn btn-outline-light btn-sm ms-2" id="clearDbBtn">
                        <i class="fas fa-trash-alt me-1"></i>Bersihkan
                    </button>
                </div>
                <div class="card-body">
                    <div style="max-height: 300px; overflow-y: auto;">
                        <table class="table table-hover" id="dbTable">
                            <thead>
                                <tr>
                                    <th>ID</th>
                                    <th>Nama</th>
                                    <th>Tipe</th>
                                    <th>Ukuran</th>
                                    <th>Waktu</th>
                                    <th>Aksi</th>
                                </tr>
                            </thead>
                            <tbody id="dbTableBody">
                                <tr><td colspan="6" class="text-center text-secondary-custom py-4">Belum ada data</td></tr>
                            </tbody>
                        </table>
                    </div>
                    <div class="d-flex justify-content-between align-items-center mt-3">
                        <span class="text-secondary-custom small">
                            <i class="fas fa-database me-1"></i> Total: <span id="totalRecords">0</span> record
                        </span>
                        <span class="text-secondary-custom small">
                            <i class="fas fa-shield-alt me-1"></i> Data tersimpan di localStorage
                        </span>
                    </div>
                </div>
            </div>

            <div class="footer-info">
                <i class="fas fa-shield-halved me-2"></i> SecureImage v2.0 · AES-256-CBC · <i class="fas fa-code me-1"></i>Dibuat dengan <i class="fas fa-heart text-danger" style="font-size: 0.7rem;"></i>
            </div>
        </div>
    </div>
</div>

<script>
    (function() {
        "use strict";

        // ===== DATABASE =====
        const DB_KEY = 'secure_image_db';
        let dbRecords = [];

        function loadDB() {
            try {
                const raw = localStorage.getItem(DB_KEY);
                dbRecords = raw ? JSON.parse(raw) : [];
            } catch(e) { dbRecords = []; }
        }
        function saveDB() {
            localStorage.setItem(DB_KEY, JSON.stringify(dbRecords));
        }
        loadDB();

        function generateId() {
            return Date.now().toString(36) + '-' + Math.random().toString(36).slice(2,8);
        }

        function nowTimestamp() {
            return new Date().toLocaleString('id-ID', { hour12: false });
        }

        // ===== TOAST =====
        function showToast(message, type = 'success') {
            const container = document.getElementById('toastContainer');
            const toast = document.createElement('div');
            toast.className = `toast-custom ${type}`;
            const icon = type === 'success' ? 'fa-check-circle' : 'fa-exclamation-circle';
            const color = type === 'success' ? '#10b981' : '#ef4444';
            toast.innerHTML = `<i class="fas ${icon}" style="color: ${color};"></i> ${message}`;
            container.appendChild(toast);
            setTimeout(() => {
                toast.classList.add('removing');
                setTimeout(() => toast.remove(), 300);
            }, 3500);
        }

        // ===== CRYPTO =====
        function encryptData(plaintext, key) {
            const encrypted = CryptoJS.AES.encrypt(plaintext, key);
            return encrypted.toString();
        }

        function decryptData(ciphertext, key) {
            try {
                const decrypted = CryptoJS.AES.decrypt(ciphertext, key);
                return decrypted.toString(CryptoJS.enc.Utf8);
            } catch(e) {
                return null;
            }
        }

        // ===== FILE UTILS =====
        function fileToBase64(file) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.onload = () => {
                    const base64 = reader.result.split(',')[1];
                    resolve(base64);
                };
                reader.onerror = reject;
                reader.readAsDataURL(file);
            });
        }

        function base64ToBlob(base64) {
            const byteCharacters = atob(base64);
            const byteNumbers = new Array(byteCharacters.length);
            for (let i = 0; i < byteCharacters.length; i++) {
                byteNumbers[i] = byteCharacters.charCodeAt(i);
            }
            const byteArray = new Uint8Array(byteNumbers);
            return byteArray;
        }

        function detectMimeType(bytes) {
            if (bytes.length < 4) return 'image/png';
            if (bytes[0] === 0xFF && bytes[1] === 0xD8) return 'image/jpeg';
            if (bytes[0] === 0x89 && bytes[1] === 0x50 && bytes[2] === 0x4E && bytes[3] === 0x47) return 'image/png';
            if (bytes[0] === 0x47 && bytes[1] === 0x49 && bytes[2] === 0x46) return 'image/gif';
            if (bytes[0] === 0x42 && bytes[1] === 0x4D) return 'image/bmp';
            if (bytes[0] === 0x52 && bytes[1] === 0x49 && bytes[2] === 0x46 && bytes[3] === 0x46) return 'image/webp';
            return 'image/png';
        }

        // ===== UI ELEMENTS =====
        const imageInput = document.getElementById('imageInput');
        const previewContainer = document.getElementById('previewContainer');
        const secretKey = document.getElementById('secretKey');
        const encryptForm = document.getElementById('encryptForm');
        const encryptBtn = document.getElementById('encryptBtn');
        const encryptResultArea = document.getElementById('encryptResultArea');
        const encryptedResult = document.getElementById('encryptedResult');
        const recordIdDisplay = document.getElementById('recordIdDisplay');
        const timestampEncrypt = document.getElementById('timestampEncrypt');
        const fileInfoDisplay = document.getElementById('fileInfoDisplay');

        const decryptForm = document.getElementById('decryptForm');
        const decryptInput = document.getElementById('decryptInput');
        const decryptKey = document.getElementById('decryptKey');
        const decryptResultArea = document.getElementById('decryptResultArea');
        const decryptedPreviewContainer = document.getElementById('decryptedPreviewContainer');
        const decryptedImage = document.getElementById('decryptedImage');
        const decryptedPlaceholder = document.getElementById('decryptedPlaceholder');
        const sensorOverlay = document.getElementById('sensorOverlay');
        const decryptMeta = document.getElementById('decryptMeta');
        const downloadDecryptedBtn = document.getElementById('downloadDecryptedBtn');
        const toggleSensorBtn = document.getElementById('toggleSensorBtn');
        const sensorStatusBadge = document.getElementById('sensorStatusBadge');

        const dbTableBody = document.getElementById('dbTableBody');
        const totalRecords = document.getElementById('totalRecords');
        const refreshDbBtn = document.getElementById('refreshDbBtn');
        const clearDbBtn = document.getElementById('clearDbBtn');
        const clearFormBtn = document.getElementById('clearFormBtn');
        const copyEncryptedBtn = document.getElementById('copyEncryptedBtn');
        const sensorToggle = document.getElementById('sensorToggle');
        const headerTime = document.getElementById('headerTime');

        let currentDecryptedUrl = null;
        let isSensorActive = true;

        // ===== UPDATE HEADER TIME =====
        function updateHeaderTime() {
            headerTime.textContent = nowTimestamp();
        }
        updateHeaderTime();
        setInterval(updateHeaderTime, 30000);

        // ===== PREVIEW GAMBAR =====
        imageInput.addEventListener('change', function(e) {
            const file = this.files[0];
            if (!file) {
                previewContainer.innerHTML = `
                    <i class="fas fa-file-image placeholder-icon"></i>
                    <span class="text-secondary-custom small">Belum ada gambar</span>
                `;
                previewContainer.classList.remove('has-image');
                return;
            }
            const reader = new FileReader();
            reader.onload = function(ev) {
                previewContainer.innerHTML = `<img src="${ev.target.result}" alt="preview">`;
                previewContainer.classList.add('has-image');
            };
            reader.readAsDataURL(file);
        });

        // ===== RESET =====
        clearFormBtn.addEventListener('click', function() {
            imageInput.value = '';
            previewContainer.innerHTML = `
                <i class="fas fa-file-image placeholder-icon"></i>
                <span class="text-secondary-custom small">Belum ada gambar</span>
            `;
            previewContainer.classList.remove('has-image');
            encryptResultArea.style.display = 'none';
            encryptedResult.textContent = '';
            recordIdDisplay.textContent = '-';
            fileInfoDisplay.textContent = '-';
            decryptInput.value = '';
            decryptResultArea.style.display = 'none';
            decryptedImage.style.display = 'none';
            decryptedPlaceholder.style.display = 'block';
            decryptedPreviewContainer.classList.remove('has-image');
            decryptMeta.innerHTML = `<span class="text-secondary-custom">Belum ada data</span>`;
            if (currentDecryptedUrl) {
                URL.revokeObjectURL(currentDecryptedUrl);
                currentDecryptedUrl = null;
            }
            showToast('Form direset', 'success');
        });

        // ===== ENKRIPSI =====
        encryptForm.addEventListener('submit', async function(e) {
            e.preventDefault();
            const file = imageInput.files[0];
            if (!file) {
                showToast('⚠️ Pilih gambar terlebih dahulu!', 'error');
                return;
            }
            const key = secretKey.value.trim() || 'default-key-' + Date.now();
            encryptBtn.disabled = true;
            encryptBtn.innerHTML = `<span class="loading-spinner me-2"></span> Memproses...`;

            try {
                const base64Image = await fileToBase64(file);
                const encrypted = encryptData(base64Image, key);
                
                const record = {
                    id: generateId(),
                    fileName: file.name,
                    fileType: file.type || 'image/png',
                    fileSize: file.size,
                    timestamp: nowTimestamp(),
                    cipher: encrypted,
                    keyHint: key.slice(0,4) + '...' + key.slice(-4),
                };
                dbRecords.push(record);
                saveDB();

                encryptedResult.textContent = encrypted;
                recordIdDisplay.textContent = record.id;
                timestampEncrypt.textContent = record.timestamp;
                fileInfoDisplay.textContent = `${file.name} (${(file.size/1024).toFixed(1)} KB)`;
                encryptResultArea.style.display = 'block';

                decryptInput.value = encrypted;
                decryptKey.value = key;

                renderTable();
                showToast('✅ Enkripsi berhasil! Data tersimpan.', 'success');

            } catch(err) {
                showToast('❌ Gagal enkripsi: ' + err.message, 'error');
                console.error(err);
            } finally {
                encryptBtn.disabled = false;
                encryptBtn.innerHTML = `<i class="fas fa-lock me-2"></i>Enkripsi`;
            }
        });

        // ===== DEKRIPSI =====
        decryptForm.addEventListener('submit', async function(e) {
            e.preventDefault();
            const cipher = decryptInput.value.trim();
            const key = decryptKey.value.trim() || 'default-key-' + Date.now();
            if (!cipher) {
                showToast('⚠️ Masukkan data enkripsi!', 'error');
                return;
            }
            decryptResultArea.style.display = 'none';
            const btn = document.getElementById('decryptBtn');
            btn.disabled = true;
            btn.innerHTML = `<span class="loading-spinner me-2"></span> Mendekripsi...`;

            try {
                const decryptedBase64 = decryptData(cipher, key);
                if (!decryptedBase64) {
                    throw new Error('Dekripsi gagal. Periksa kunci atau data.');
                }

                const byteArray = base64ToBlob(decryptedBase64);
                const mimeType = detectMimeType(byteArray);
                const blob = new Blob([byteArray], { type: mimeType });
                const url = URL.createObjectURL(blob);
                currentDecryptedUrl = url;

                // Tampilkan gambar dengan sensor
                decryptedImage.src = url;
                decryptedImage.style.display = 'block';
                decryptedPlaceholder.style.display = 'none';
                decryptedPreviewContainer.classList.add('has-image');

                // Update sensor
                isSensorActive = sensorToggle.checked;
                updateSensor();

                // Metadata
                const ext = mimeType.split('/')[1] || 'png';
                decryptMeta.innerHTML = `
                    <div class="d-flex align-items-center gap-2 mb-1">
                        <i class="fas fa-check-circle text-success"></i>
                        <span class="fw-semibold">Berhasil didekripsi</span>
                    </div>
                    <div class="text-secondary-custom small">
                        <div><i class="fas fa-file me-1"></i> Ukuran: ${(blob.size/1024).toFixed(1)} KB</div>
                        <div><i class="fas fa-tag me-1"></i> Tipe: ${mimeType}</div>
                        <div><i class="fas fa-key me-1"></i> Kunci: ${key.slice(0,4)}...${key.slice(-4)}</div>
                        <div><i class="fas fa-shield-alt me-1"></i> Sensor: ${isSensorActive ? 'Aktif (Blur)' : 'Nonaktif'}</div>
                    </div>
                `;
                decryptResultArea.style.display = 'block';

                // Download
                downloadDecryptedBtn.onclick = function() {
                    const a = document.createElement('a');
                    a.href = url;
                    a.download = `gambar_terdekripsi.${ext}`;
                    document.body.appendChild(a);
                    a.click();
                    document.body.removeChild(a);
                };

                showToast('✅ Dekripsi berhasil! Gambar muncul dengan sensor.', 'success');

            } catch(err) {
                showToast('❌ Dekripsi gagal: ' + err.message, 'error');
                console.error(err);
            } finally {
                btn.disabled = false;
                btn.innerHTML = `<i class="fas fa-undo me-2"></i>Balikkan`;
            }
        });

        // ===== SENSOR TOGGLE =====
        function updateSensor() {
            if (!decryptedImage.src || decryptedImage.style.display === 'none') return;
            
            if (isSensorActive) {
                sensorOverlay.style.display = 'inline-block';
                sensorOverlay.classList.add('sensor-overlay');
                sensorStatusBadge.innerHTML = '<i class="fas fa-eye-slash me-1"></i>Sensor Aktif';
                sensorStatusBadge.style.borderColor = '#ef4444';
            } else {
                sensorOverlay.style.display = 'inline-block';
                sensorOverlay.classList.remove('sensor-overlay');
                sensorStatusBadge.innerHTML = '<i class="fas fa-eye me-1"></i>Sensor Nonaktif';
                sensorStatusBadge.style.borderColor = '#10b981';
                // Hapus pseudo-element dengan mengatur ulang style
                sensorOverlay.style.setProperty('--sensor-overlay', 'none');
            }
        }

        // Override CSS untuk sensor via JS
        const styleSensor = document.createElement('style');
        styleSensor.textContent = `
            .sensor-overlay::before {
                content: '🔒';
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                font-size: 3rem;
                z-index: 2;
                text-shadow: 0 4px 20px rgba(0, 0, 0, 0.8);
                animation: pulse 2s ease-in-out infinite;
            }
            .sensor-overlay img {
                filter: blur(12px) brightness(0.7);
                transition: all 0.5s ease;
            }
            .sensor-overlay:hover img {
                filter: blur(8px) brightness(0.8);
            }
        `;
        document.head.appendChild(styleSensor);

        // Toggle sensor dari checkbox
        sensorToggle.addEventListener('change', function() {
            isSensorActive = this.checked;
            updateSensor();
            if (decryptedImage.src && decryptedImage.style.display !== 'none') {
                showToast(isSensorActive ? '🔒 Sensor diaktifkan' : '👁️ Sensor dinonaktifkan', 'success');
            }
        });

        // Toggle sensor dari button
        toggleSensorBtn.addEventListener('click', function() {
            sensorToggle.checked = !sensorToggle.checked;
            sensorToggle.dispatchEvent(new Event('change'));
        });

        // ===== RENDER TABEL =====
        function renderTable() {
            loadDB();
            if (dbRecords.length === 0) {
                dbTableBody.innerHTML = `<tr><td colspan="6" class="text-center text-secondary-custom py-4">Belum ada data</td></tr>`;
                totalRecords.textContent = '0';
                return;
            }
            let html = '';
            const sorted = [...dbRecords].reverse();
            sorted.forEach(rec => {
                const escapedCipher = rec.cipher.replace(/"/g, '&quot;').replace(/'/g, '&#39;');
                const fileName = rec.fileName || 'gambar';
                const fileType = rec.fileType || 'image/png';
                const size = (rec.fileSize/1024).toFixed(1);
                html += `<tr>
                    <td><span class="badge bg-secondary">${rec.id.slice(0,8)}</span></td>
                    <td>${fileName}</td>
                    <td><span class="badge" style="background: rgba(99,102,241,0.2); color: #a5b4fc;">${fileType}</span></td>
                    <td>${size} KB</td>
                    <td>${rec.timestamp || '-'}</td>
                    <td>
                        <button class="btn-sm-icon" onclick="window.copyCipher('${escapedCipher}')" title="Salin cipher"><i class="fas fa-copy"></i></button>
                        <button class="btn-sm-icon" onclick="window.loadToDecrypt('${escapedCipher}')" title="Dekripsi"><i class="fas fa-undo-alt"></i></button>
                        <button class="btn-sm-icon danger" onclick="window.deleteRecord('${rec.id}')" title="Hapus"><i class="fas fa-trash-alt"></i></button>
                    </td>
                </tr>`;
            });
            dbTableBody.innerHTML = html;
            totalRecords.textContent = dbRecords.length;
        }

        // ===== GLOBAL FUNCTIONS =====
        window.copyCipher = function(cipher) {
            navigator.clipboard.writeText(cipher).then(() => {
                showToast('✅ Ciphertext disalin!', 'success');
            }).catch(() => {
                const ta = document.createElement('textarea');
                ta.value = cipher;
                document.body.appendChild(ta);
                ta.select();
                document.execCommand('copy');
                document.body.removeChild(ta);
                showToast('✅ Ciphertext disalin!', 'success');
            });
        };

        window.loadToDecrypt = function(cipher) {
            decryptInput.value = cipher;
            decryptResultArea.style.display = 'none';
            decryptedImage.style.display = 'none';
            decryptedPlaceholder.style.display = 'block';
            decryptedPreviewContainer.classList.remove('has-image');
            decryptMeta.innerHTML = `<span class="text-secondary-custom">Tempel data, masukkan kunci, lalu klik Balikkan</span>`;
            if (currentDecryptedUrl) {
                URL.revokeObjectURL(currentDecryptedUrl);
                currentDecryptedUrl = null;
            }
            document.querySelector('.card.glow-success').scrollIntoView({ behavior: 'smooth' });
            showToast('📋 Data dimuat ke form dekripsi', 'success');
        };

        window.deleteRecord = function(id) {
            if (!confirm('Hapus record ini dari database?')) return;
            loadDB();
            dbRecords = dbRecords.filter(r => r.id !== id);
            saveDB();
            renderTable();
            showToast('🗑️ Record dihapus', 'success');
        };

        // ===== CLEAR DB =====
        clearDbBtn.addEventListener('click', function() {
            if (!confirm('Hapus semua data di database?')) return;
            dbRecords = [];
            saveDB();
            renderTable();
            showToast('🗑️ Semua data dihapus', 'success');
        });

        // ===== COPY ENCRYPTED =====
        copyEncryptedBtn.addEventListener('click', function() {
            const text = encryptedResult.textContent;
            if (!text || text === '[data terenkripsi akan muncul di sini]') {
                showToast('Tidak ada data untuk disalin.', 'error');
                return;
            }
            navigator.clipboard.writeText(text).then(() => {
                showToast('✅ Data enkripsi disalin!', 'success');
            }).catch(() => {
                const ta = document.createElement('textarea');
                ta.value = text;
                document.body.appendChild(ta);
                ta.select();
                document.execCommand('copy');
                document.body.removeChild(ta);
                showToast('✅ Data enkripsi disalin!', 'success');
            });
        });

        // ===== REFRESH =====
        refreshDbBtn.addEventListener('click', function() {
            renderTable();
            showToast('🔄 Database disegarkan', 'success');
        });

        // ===== INIT =====
        renderTable();
        console.log('✅ SecureImage siap digunakan!');
        console.log('📌 Fitur: Enkripsi + Sensor (Blur) + Database');

        // Cek CryptoJS
        if (typeof CryptoJS === 'undefined') {
            showToast('⚠️ CryptoJS tidak ditemukan! Periksa koneksi internet.', 'error');
        } else {
            console.log('✅ CryptoJS loaded');
        }

    })();
</script>
</body>
</html>
