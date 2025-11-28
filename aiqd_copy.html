<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>双目眼底智能诊断系统</title>

  <!-- Tailwind -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome -->
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">

  <!-- Tailwind 自定义配置 -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#1E88E5',
            secondary: '#FF69B4',
            neutral: {
              100: '#F5F7FA',
              200: '#E4E7EB',
              300: '#CBD2D9',
              800: '#333333',
              600: '#666666',
              400: '#999999',
            }
          },
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
          boxShadow: {
            'card': '0 2px 8px rgba(0, 0, 0, 0.08)',
          }
        },
      }
    }
  </script>

  <!-- Tailwind 工具类拓展 -->
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto {
        content-visibility: auto;
      }
      .slider-thumb {
        @apply appearance-none w-6 h-6 rounded-full bg-primary cursor-pointer shadow-md;
      }
      .slider-track {
        @apply h-2 rounded-full bg-neutral-300;
      }
      .btn-primary {
        @apply bg-primary text-white font-medium py-2 px-4 rounded-md hover:bg-primary/90 transition-all duration-300 focus:outline-none focus:ring-2 focus:ring-primary/50;
      }
      .btn-base {
        @apply w-full font-semibold rounded-md py-3 text-lg transition-all duration-300 focus:outline-none focus:ring-2 focus:ring-primary/30;
      }
      .btn-enabled {
        @apply bg-primary text-white shadow-lg hover:bg-primary/90 cursor-pointer;
      }
      .btn-disabled {
        @apply bg-neutral-300 text-neutral-500 cursor-not-allowed;
      }
      .card-container {
        @apply bg-white border border-neutral-200 rounded-lg shadow-card p-4;
      }
    }
  </style>

  <!-- 其它样式 -->
  <style>
    .auto-toggle-row {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      gap: 10px;
      margin-top: -4px;
    }
    .auto-toggle-label {
      font-size: 1.25rem;
      font-weight: 400;
      color: #1f2a37;
      user-select: none;
    }
    .auto-switch {
      width: 36px;
      height: 22px;
      border-radius: 999px;
      background-color: #d7dde8;
      border: none;
      position: relative;
      cursor: pointer;
      transition: background-color 0.2s ease;
    }
    .auto-switch::after {
      content: "";
      width: 16px;
      height: 16px;
      border-radius: 50%;
      background: #fff;
      position: absolute;
      top: 3px;
      left: 3px;
      box-shadow: 0 2px 6px rgba(15, 23, 42, 0.2);
      transition: transform 0.2s ease;
    }
    .auto-switch-on {
      background-color: #1e88e5;
    }
    .auto-switch-on::after {
      transform: translateX(14px);
    }

    /* range 美化 + 渐变背景 */
    input[type="range"] {
      -webkit-appearance: none;
      appearance: none;
      width: 100%;
      background: transparent;
      border-radius: 999px;
      height: 8px;
    }
    input[type="range"]::-webkit-slider-runnable-track {
      height: 8px;
      border-radius: 999px;
      background-color: transparent;
    }
    input[type="range"]::-webkit-slider-thumb {
      -webkit-appearance: none;
      appearance: none;
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background-color: #1E88E5;
      margin-top: -6px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.3);
      cursor: pointer;
    }
    input[type="range"]::-moz-range-track {
      height: 8px;
      border-radius: 999px;
      background-color: transparent;
    }
    input[type="range"]::-moz-range-thumb {
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background-color: #1E88E5;
      border: none;
      box-shadow: 0 2px 6px rgba(0,0,0,0.3);
      cursor: pointer;
    }
  </style>
</head>
<body class="bg-neutral-100 font-sans text-neutral-600 min-h-screen flex flex-col">
  <!-- 头部 -->
  <header class="bg-white border-b-2 border-neutral-200 h-14 flex items-center px-6 sticky top-0 z-10">
    <div class="flex items-center space-x-3">
      <div class="w-7 h-7 rounded-full bg-primary flex items-center justify-center">
        <i class="fa fa-plus text-white text-xs"></i>
      </div>
      <span class="font-bold text-neutral-800 text-lg">智绘医疗</span>
    </div>
    <div class="flex-1 text-center">
      <h1 class="font-bold text-neutral-800 text-lg md:text-xl">双目眼底智能诊断系统</h1>
    </div>
    <div class="flex space-x-2">
      <button id="lang-zh" class="btn-primary text-sm px-3 py-1">中文</button>
      <button id="lang-en" class="bg-white text-neutral-600 border border-neutral-200 rounded-md text-sm px-3 py-1 hover:bg-neutral-100 transition-all">EN</button>
    </div>
  </header>

  <!-- 主体 -->
  <main class="flex-1 p-4 md:p-6 flex flex-col lg:flex-row gap-6">
    <!-- 左眼 -->
    <section class="card-container flex-1 min-w-[300px] flex flex-col">
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-2xl font-bold text-neutral-800" data-lang="left-eye">左眼眼底图像</h2>
        <label for="left-upload" class="btn-primary text-lg px-4 py-2 cursor-pointer">
          <i class="fa fa-upload mr-2"></i><span data-lang="upload">上传</span>
        </label>
        <input type="file" id="left-upload" accept="image/*" class="hidden">
      </div>
      <div id="left-preview" class="border border-neutral-200 rounded-md bg-white min-h-[400px] flex items-center justify-center mb-4 overflow-hidden relative">
        <div class="preview-placeholder absolute inset-0 flex flex-col items-center justify-center text-neutral-300">
          <i class="fa fa-image text-4xl mb-3"></i>
          <p class="text-base">上传图像以预览</p>
        </div>
        <img id="left-image" class="max-w-full max-h-[400px] object-contain z-10 hidden" alt="左眼眼底图像">
      </div>
      <div class="flex flex-col gap-4">
        <div class="flex items-center gap-3">
          <label for="left-brightness" class="text-xl text-neutral-800 w-24" data-lang="brightness">亮度</label>
          <input type="range" id="left-brightness" min="0" max="200" value="100" class="flex-1 slider-track">
          <span id="left-brightness-value" class="text-neutral-600 w-10 text-center">100</span>
        </div>
        <div class="flex items-center gap-3">
          <label for="left-contrast" class="text-xl text-neutral-800 w-24" data-lang="contrast">对比度</label>
          <input type="range" id="left-contrast" min="0" max="200" value="100" class="flex-1 slider-track">
          <span id="left-contrast-value" class="text-neutral-600 w-10 text-center">100</span>
        </div>
        <div class="auto-toggle-row">
          <span class="auto-toggle-label">自适应</span>
          <button type="button" class="auto-switch" data-auto-switch="left" aria-pressed="false"></button>
        </div>
      </div>
    </section>

    <!-- 右眼 -->
    <section class="card-container flex-1 min-w-[300px] flex flex-col">
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-2xl font-bold text-neutral-800" data-lang="right-eye">右眼眼底图像</h2>
        <label for="right-upload" class="btn-primary text-lg px-4 py-2 cursor-pointer">
          <i class="fa fa-upload mr-2"></i><span data-lang="upload">上传</span>
        </label>
        <input type="file" id="right-upload" accept="image/*" class="hidden">
      </div>
      <div id="right-preview" class="border border-neutral-200 rounded-md bg-white min-h-[400px] flex items-center justify-center mb-4 overflow-hidden relative">
        <div class="preview-placeholder absolute inset-0 flex flex-col items-center justify-center text-neutral-300">
          <i class="fa fa-image text-4xl mb-3"></i>
          <p class="text-base">上传图像以预览</p>
        </div>
        <img id="right-image" class="max-w-full max-h-[400px] object-contain z-10 hidden" alt="右眼眼底图像">
      </div>
      <div class="flex flex-col gap-4">
        <div class="flex items-center gap-3">
          <label for="right-brightness" class="text-xl text-neutral-800 w-24" data-lang="brightness">亮度</label>
          <input type="range" id="right-brightness" min="0" max="200" value="100" class="flex-1 slider-track">
          <span id="right-brightness-value" class="text-neutral-600 w-10 text-center">100</span>
        </div>
        <div class="flex items-center gap-3">
          <label for="right-contrast" class="text-xl text-neutral-800 w-24" data-lang="contrast">对比度</label>
          <input type="range" id="right-contrast" min="0" max="200" value="100" class="flex-1 slider-track">
          <span id="right-contrast-value" class="text-neutral-600 w-10 text-center">100</span>
        </div>
        <div class="auto-toggle-row">
          <span class="auto-toggle-label">自适应</span>
          <button type="button" class="auto-switch" data-auto-switch="right" aria-pressed="false"></button>
        </div>
      </div>
    </section>

    <!-- 诊断结果 -->
    <section class="card-container lg:w-[320px] flex flex-col gap-6">
      <button id="predict-btn" class="btn-base btn-disabled" disabled>
        <i class="fa fa-stethoscope mr-2"></i><span data-lang="predict">一键预测</span>
      </button>

      <div class="space-y-4">
        <div>
          <div class="flex items-center text-neutral-800 font-bold text-lg" data-lang="predict-result">
            <i class="fa fa-clock-o text-primary mr-2"></i>预测结果
          </div>
          <p class="text-sm text-neutral-400 mt-1" id="prediction-subtitle">暂无预测结果</p>
        </div>
        <div id="probability-list" class="space-y-3">
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">糖尿病</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="diabetes">--</span>
          </div>
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">青光眼</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="glaucoma">--</span>
          </div>
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">白内障</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="cataract">--</span>
          </div>
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">AMD</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="amd">--</span>
          </div>
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">高血压</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="hypertension">--</span>
          </div>
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">近视</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="myopia">--</span>
          </div>
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">其它疾病 / 异常</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="others">--</span>
          </div>
          <div class="flex items-center justify-between p-3 border border-neutral-200 rounded-md">
            <span class="text-neutral-700">一致性检验</span>
            <span class="px-3 py-1 rounded-full bg-primary/10 text-primary font-semibold text-sm prob-badge opacity-30" data-prob-key="scores">--</span>
          </div>
        </div>
      </div>

      <div class="border-t border-neutral-200 pt-4 mt-2 space-y-3">
        <h3 class="flex items-center text-neutral-800 font-bold text-lg" data-lang="report">
          <i class="fa fa-file-text-o text-primary mr-2"></i>诊断报告
        </h3>
        <div id="report-content" class="bg-neutral-100 rounded-md p-4 min-h-[200px] text-neutral-400 text-sm leading-relaxed">
          上传双眼图像并点击“一键预测”后，将生成详细诊断报告
        </div>
      </div>
    </section>
  </main>

  <!-- 弹出图片 Modal：放大 + 四图布局 -->
  <div id="result-modal" class="fixed inset-0 bg-black/50 flex items-center justify-center z-50 hidden">
    <div class="bg-white rounded-lg shadow-xl max-w-4xl w-[95%] p-5 relative">
      <!-- 右上角关闭 -->
      <button id="modal-close" type="button"
              class="absolute top-3 right-3 text-neutral-400 hover:text-neutral-700">
        <i class="fa fa-times text-lg"></i>
      </button>
      <h4 class="text-lg font-semibold mb-4 text-neutral-800">
        <span data-lang="popup-title">AI诊断提示</span>
      </h4>

      <!-- 四张图 2x2 -->
      <div class="grid grid-cols-2 gap-4 mb-4">
      <!-- 左上：左眼原型图 -->
      <figure class="flex flex-col items-center">
        <img
          id="modal-left-proto"
          src="left_eye_iv_A.png"  
          alt="左眼原型图"
          class="w-full max-h-[35vh] object-contain rounded-md border border-neutral-200"
        >
        <figcaption class="mt-2 text-sm text-neutral-600" data-lang="caption-left-proto">
          左眼原型图
        </figcaption>
      </figure>

      <!-- 右上：右眼原型图 -->
      <figure class="flex flex-col items-center">
        <img
          id="modal-right-proto"
          src="right_eye_iv_A.png"
          alt="右眼原型图"
          class="w-full max-h-[35vh] object-contain rounded-md border border-neutral-200"
        >
        <figcaption class="mt-2 text-sm text-neutral-600" data-lang="caption-right-proto">
          右眼原型图
        </figcaption>
      </figure>

      <!-- 左下：左眼激活图 -->
      <figure class="flex flex-col items-center">
        <img
          id="modal-left-activation"
          src="left_eye_relu_A.png"
          alt="左眼激活图"
          class="w-full max-h-[35vh] object-contain rounded-md border border-neutral-200"
        >
        <figcaption class="mt-2 text-sm text-neutral-600" data-lang="caption-left-activation">
          左眼激活图
        </figcaption>
      </figure>

      <!-- 右下：右眼激活图 -->
      <figure class="flex flex-col items-center">
        <img
          id="modal-right-activation"
          src="right_eye_relu_A.png"
          alt="右眼激活图"
          class="w-full max-h-[35vh] object-contain rounded-md border border-neutral-200"
        >
        <figcaption class="mt-2 text-sm text-neutral-600" data-lang="caption-right-activation">
          右眼激活图
        </figcaption>
      </figure>

      </div>

      <button id="modal-back" type="button"
              class="btn-base bg-primary text-white text-base py-2 mt-1">
        <span data-lang="popup-back">返回</span>
      </button>
    </div>
  </div>

  <!-- 页脚 -->
  <footer class="bg-white border-t border-neutral-200 py-4 px-6 text-center text-neutral-400 text-sm">
    <p data-lang="copyright">© 2025 智绘医疗 版权所有 | 双目眼底智能诊断系统 V1.0</p>
  </footer>

  <!-- JS -->
  <script>
    document.addEventListener('DOMContentLoaded', function () {
      /************ 语言切换 ************/
      const langZhBtn = document.getElementById('lang-zh');
      const langEnBtn = document.getElementById('lang-en');
      const translations = {
        'left-eye': { zh: '左眼眼底图像', en: 'Left Eye Fundus Image' },
        'right-eye': { zh: '右眼眼底图像', en: 'Right Eye Fundus Image' },
        'upload': { zh: '上传', en: 'Upload' },
        'brightness': { zh: '亮度', en: 'Brightness' },
        'contrast': { zh: '对比度', en: 'Contrast' },
        'func-title': { zh: '系统功能展示', en: 'System Function Demo' },
        'func-desc': { zh: '双原型学习驱动的眼底增强分布诊断与报告系统', en: 'Dual Prototype Learning Driven Fundus Enhancement Distribution Diagnosis and Reporting System' },
        'predict': { zh: '一键预测', en: 'One-Click Predict' },
        'predict-result': { zh: '预测结果', en: 'Prediction Result' },
        'predict-hint': { zh: 'AMD / 糖尿病 / 有髓神经纤维', en: 'AMD / Diabetes / Myelinated Nerve Fiber' },
        'disease1': { zh: '糖尿病视网膜病变', en: 'Diabetic Retinopathy' },
        'disease2': { zh: '青光眼', en: 'Glaucoma' },
        'disease3': { zh: '白内障', en: 'Cataract' },
        'disease4': { zh: '黄斑病变', en: 'Macular Degeneration' },
        'disease5': { zh: '视网膜脱离', en: 'Retinal Detachment' },
        'disease6': { zh: '高血压视网膜病变', en: 'Hypertensive Retinopathy' },
        'disease7': { zh: '正常眼底', en: 'Normal Fundus' },
        'report': { zh: '诊断报告', en: 'Diagnostic Report' },
        'report-placeholder': {
          zh: '上传双眼图像并点击"一键预测"后，将生成详细诊断报告',
          en: 'Upload fundus images of both eyes and click "One-Click Predict" to generate a detailed diagnostic report'
        },
        'popup-title': {
          zh: 'AI诊断提示',
          en: 'AI Diagnostic Hint'
        },
        'popup-back': {
          zh: '返回',
          en: 'Back'
        },
        'caption-left-proto': {
          zh: '左眼原型图',
          en: 'Left Eye Prototype'
        },
        'caption-left-activation': {
          zh: '左眼激活图',
          en: 'Left Eye Activation Map'
        },
        'caption-right-proto': {
          zh: '右眼原型图',
          en: 'Right Eye Prototype'
        },
        'caption-right-activation': {
          zh: '右眼激活图',
          en: 'Right Eye Activation Map'
        },
        'copyright': {
          zh: '© 2025 智绘医疗 版权所有 | 双目眼底智能诊断系统 V1.0',
          en: '© 2025 Zhihui Medical. All Rights Reserved | Binocular Fundus Intelligent Diagnosis System V1.0'
        }
      };

      function updateLanguage(lang) {
        document.querySelectorAll('[data-lang]').forEach(el => {
          const key = el.getAttribute('data-lang');
          if (translations[key] && translations[key][lang]) {
            el.textContent = translations[key][lang];
          }
        });
        document.documentElement.lang = lang;
      }

      const getCurrentLang = () => {
        const lang = document.documentElement.lang || 'zh';
        return lang.toLowerCase().startsWith('zh') ? 'zh' : 'en';
      };

      // 初始化语言
      updateLanguage('zh');
      langZhBtn.classList.add('bg-primary', 'text-white');
      langZhBtn.classList.remove('bg-white', 'text-neutral-600', 'border', 'border-neutral-200');
      langEnBtn.classList.remove('bg-primary', 'text-white');
      langEnBtn.classList.add('bg-white', 'text-neutral-600', 'border', 'border-neutral-200');

      langZhBtn.addEventListener('click', () => {
        langZhBtn.classList.add('bg-primary', 'text-white');
        langZhBtn.classList.remove('bg-white', 'text-neutral-600', 'border', 'border-neutral-200');
        langEnBtn.classList.remove('bg-primary', 'text-white');
        langEnBtn.classList.add('bg-white', 'text-neutral-600', 'border', 'border-neutral-200');
        updateLanguage('zh');
        if (predictionGenerated) {
          renderPredictionOutput('zh');
        } else {
          resetPredictionOutput('zh');
        }
      });

      langEnBtn.addEventListener('click', () => {
        langEnBtn.classList.add('bg-primary', 'text-white');
        langEnBtn.classList.remove('bg-white', 'text-neutral-600', 'border', 'border-neutral-200');
        langZhBtn.classList.remove('bg-primary', 'text-white');
        langZhBtn.classList.add('bg-white', 'text-neutral-600', 'border', 'border-neutral-200');
        updateLanguage('en');
        if (predictionGenerated) {
          renderPredictionOutput('en');
        } else {
          resetPredictionOutput('en');
        }
      });

      /************ DOM 引用 ************/
      const leftUpload = document.getElementById('left-upload');
      const rightUpload = document.getElementById('right-upload');
      const leftImage = document.getElementById('left-image');
      const rightImage = document.getElementById('right-image');
      const leftPreview = document.getElementById('left-preview');
      const rightPreview = document.getElementById('right-preview');
      const predictBtn = document.getElementById('predict-btn');
      const reportContent = document.getElementById('report-content');
      const predictionSubtitle = document.getElementById('prediction-subtitle');
      const probabilityBadges = document.querySelectorAll('[data-prob-key]');
      const autoSwitches = document.querySelectorAll('[data-auto-switch]');

      // Modal 相关
      const resultModal = document.getElementById('result-modal');
      const modalClose = document.getElementById('modal-close');
      const modalBack = document.getElementById('modal-back');

      // 🔹 新增：弹窗 4 张图的元素引用
      const modalLeftProto = document.getElementById('modal-left-proto');
      const modalRightProto = document.getElementById('modal-right-proto');
      const modalLeftActivation = document.getElementById('modal-left-activation');
      const modalRightActivation = document.getElementById('modal-right-activation');

      // 🔹 新增：A/B 两套图片路径
      // index 0 对应模板 A，index 1 对应模板 B（和 currentPresetIndex 对齐）
      // 🔹 新增：根据当前预测模板 A/B 更新弹窗图片
      function updateModalImages() {
        const set = modalImageSets[currentPresetIndex] || modalImageSets[0];
        if (modalLeftProto && set.leftProto) {
          modalLeftProto.src = set.leftProto;
        }
        if (modalRightProto && set.rightProto) {
          modalRightProto.src = set.rightProto;
        }
        if (modalLeftActivation && set.leftActivation) {
          modalLeftActivation.src = set.leftActivation;
        }
        if (modalRightActivation && set.rightActivation) {
          modalRightActivation.src = set.rightActivation;
        }
        }

      const modalImageSets = [
        // 模板 A
        {
          leftProto: 'left_eye_iv_A.png',
          rightProto: 'right_eye_iv_A.png',
          leftActivation: 'left_eye_relu_A.png',
          rightActivation: 'right_eye_relu_A.png'
        },
        // 模板 B
        {
          leftProto: 'left_eye_iv_B.png',
          rightProto: 'right_eye_iv_B.png',
          leftActivation: 'left_eye_relu_B.png',
          rightActivation: 'right_eye_relu_B.png'
        }
      ];
      function openResultModal() {
        if (resultModal) {
          resultModal.classList.remove('hidden');
        }
      }

      function closeResultModal() {
        if (resultModal) {
          resultModal.classList.add('hidden');
        }
      }

      if (modalClose) {
        modalClose.addEventListener('click', closeResultModal);
      }
      if (modalBack) {
        modalBack.addEventListener('click', closeResultModal);
      }
      if (resultModal) {
        resultModal.addEventListener('click', (e) => {
          if (e.target === resultModal) {
            closeResultModal();
          }
        });
      }

      const sliderMap = {
        left: {
          brightness: document.getElementById('left-brightness'),
          contrast: document.getElementById('left-contrast'),
          image: leftImage
        },
        right: {
          brightness: document.getElementById('right-brightness'),
          contrast: document.getElementById('right-contrast'),
          image: rightImage
        }
      };

      /************ 两套预测模板 ************/

      // 模板 A
      const probabilityPresetA = {
        diabetes: '0.816',
        glaucoma: '0.127',
        cataract: '0.042',
        amd: '0.874',
        hypertension: '0.293',
        myopia: '0.178',
        others: '0.919',
        scores:'0.934'
      };

      const reportTemplateZhA = `
        <div class="space-y-6 text-left text-neutral-700 leading-relaxed">
          <div>
            <p class="font-semibold text-base mb-2">1. 老年性黄斑变性（AMD）</p>
            <p class="mb-1"><strong>诊断：</strong>黄斑区退行性病变，可能出现视力下降、视物变形和视野中心暗点。</p>
            <p class="mb-1"><strong>治疗建议：</strong>中期 AMD：建议补充微量营养素（如维生素 C、维生素 E、锌等），并定期随访。</p>
            <p class="mb-1"><strong>生活方式管理：</strong>戒烟、控制血压、定期使用 Amsler 方格表监测视力变化。</p>
          </div>
          <div>
            <p class="font-semibold text-base mb-2">2. 糖尿病视网膜病变（DR）</p>
            <p class="mb-1"><strong>诊断：</strong>视网膜微血管损害，非增生型（NPDR），并发糖尿病性黄斑水肿（DME）。</p>
            <p class="mb-1"><strong>治疗建议：</strong>控制基础疾病：严格控制血糖、血压、血脂，以延缓病变进展。</p>
            <p class="mb-1"><strong>生活方式管理：</strong>均衡饮食、规律运动，遵医嘱进行眼底检查。</p>
          </div>
        </div>
      `;

      const reportTemplateEnA = `
        <div class="space-y-6 text-left text-neutral-700 leading-relaxed">
          <div>
            <p class="font-semibold text-base mb-2">1. Age-related Macular Degeneration (AMD)</p>
            <p class="mb-1"><strong>Diagnosis:</strong> Degenerative lesions at the macula with possible visual decline, metamorphopsia, and central scotoma.</p>
            <p class="mb-1"><strong>Treatment Advice:</strong> Intermediate AMD: supplement micronutrients (vitamin C, vitamin E, zinc, etc.) and schedule regular follow-ups.</p>
            <p class="mb-1"><strong>Lifestyle Management:</strong> Stop smoking, control blood pressure, and monitor vision with the Amsler grid.</p>
          </div>
          <div>
            <p class="font-semibold text-base mb-2">2. Diabetic Retinopathy (DR)</p>
            <p class="mb-1"><strong>Diagnosis:</strong> Non-proliferative retinal microvascular damage (NPDR) with diabetic macular edema (DME).</p>
            <p class="mb-1"><strong>Treatment Advice:</strong> Control systemic disease—strictly manage glucose, blood pressure, and lipids to slow progression.</p>
            <p class="mb-1"><strong>Lifestyle Management:</strong> Maintain balanced diet, regular exercise, and periodic fundus examinations as prescribed.</p>
          </div>
        </div>
      `;

      // 模板 B
      const probabilityPresetB = {
        diabetes: '0.233',
        glaucoma: '0.165',
        cataract: '0.121',
        amd: '0.112',
        hypertension: '0.503',
        myopia: '0.652',
        others: '0.278',
        scores:'0.901'
      };

      const reportTemplateZhB = `
        <div class="space-y-6 text-left text-neutral-700 leading-relaxed">
          <div>
            <p class="font-semibold text-base mb-2">1. 高度近视伴黄斑改变</p>
            <p class="mb-1"><strong>诊断：</strong>眼轴延长导致黄斑区萎缩性及变性改变，可出现视力下降、视物变形及暗影。</p>
            <p class="mb-1"><strong>治疗建议：</strong>定期进行眼底照相或OCT随访，如出现黄斑出血或新生血管需尽早就诊。</p>
            <p class="mb-1"><strong>生活方式管理：</strong>避免长时间近距离用眼，注意用眼休息，控制体重与血脂。</p>
          </div>
          <div>
            <p class="font-semibold text-base mb-2">2. 高血压视网膜病变</p>
            <p class="mb-1"><strong>诊断：</strong>视网膜动脉变细、反光增强，可伴有出血或渗出，提示全身血压控制不佳。</p>
            <p class="mb-1"><strong>治疗建议：</strong>在心内科或全科医生指导下规范降压治疗，必要时联合控制血脂及血糖。</p>
            <p class="mb-1"><strong>生活方式管理：</strong>低盐饮食、规律运动、保证睡眠，避免情绪及血压大幅波动。</p>
          </div>
        </div>
      `;

      const reportTemplateEnB = `
        <div class="space-y-6 text-left text-neutral-700 leading-relaxed">
          <div>
            <p class="font-semibold text-base mb-2">1. Pathologic Myopia with Macular Changes</p>
            <p class="mb-1"><strong>Diagnosis:</strong> Axial elongation with atrophic and degenerative changes at the macula, leading to decreased vision and metamorphopsia.</p>
            <p class="mb-1"><strong>Treatment Advice:</strong> Regular follow-up with fundus photography or OCT; urgent visit if macular hemorrhage or CNV is suspected.</p>
            <p class="mb-1"><strong>Lifestyle Management:</strong> Reduce prolonged near work, take frequent breaks, and maintain healthy body weight and lipid levels.</p>
          </div>
          <div>
            <p class="font-semibold text-base mb-2">2. Hypertensive Retinopathy</p>
            <p class="mb-1"><strong>Diagnosis:</strong> Generalized arteriolar narrowing with focal changes and possible hemorrhages/exudates, indicating suboptimal blood pressure control.</p>
            <p class="mb-1"><strong>Treatment Advice:</strong> Optimize antihypertensive regimen under physician guidance; control lipids and glucose when necessary.</p>
            <p class="mb-1"><strong>Lifestyle Management:</strong> Low-salt diet, regular exercise, good sleep, and avoidance of large blood pressure fluctuations.</p>
          </div>
        </div>
      `;

      const reportTemplateZhList = [reportTemplateZhA, reportTemplateZhB];
      const reportTemplateEnList = [reportTemplateEnA, reportTemplateEnB];
      const probabilityPresetList = [probabilityPresetA, probabilityPresetB];

      // 不同模板对应的预测副标题
      const predictionSubtitleMap = {
        zh: [
          'AMD / 糖尿病 / 有髓神经纤维',          // 模板 A
          '高度近视 / 高血压视网膜病变'            // 模板 B
        ],
        en: [
          'AMD / Diabetes / Myelinated Nerve Fiber',          // Template A
          'Pathologic Myopia / Hypertensive Retinopathy'      // Template B
        ]
      };

      // 当前使用哪一份模板：0=A，1=B
      let currentPresetIndex = 0;

      // “双眼图像配对版本号”相关
      let leftUploadCount = 0;
      let rightUploadCount = 0;
      let pairVersion = 0;
      let lastPredictedPairVersion = -1;

      let predictionGenerated = false;

      /************ 公共函数 ************/
      function setPredictButtonState(enabled) {
        if (enabled) {
          predictBtn.disabled = false;
          predictBtn.classList.add('btn-enabled');
          predictBtn.classList.remove('btn-disabled');
        } else {
          predictBtn.disabled = true;
          predictBtn.classList.remove('btn-enabled');
          predictBtn.classList.add('btn-disabled');
        }
      }

      // 初始 & 重置：没有预测结果
      function resetPredictionOutput(lang = getCurrentLang()) {
        predictionGenerated = false;

        if (predictionSubtitle) {
          predictionSubtitle.textContent =
            lang === 'zh' ? '暂无预测结果' : 'No prediction yet';
        }

        probabilityBadges.forEach(badge => {
          badge.textContent = '--';
          badge.classList.add('opacity-30');
        });

        const placeholderText = {
          zh: '上传双眼图像并点击“一键预测”后，将生成详细诊断报告',
          en: 'Upload fundus images of both eyes and click "One-Click Predict" to generate a detailed diagnostic report.'
        };
        reportContent.innerHTML = placeholderText[lang] || placeholderText.zh;
        reportContent.classList.add('text-neutral-400');
        reportContent.classList.remove('text-neutral-700');
      }

      // 有预测结果时的渲染
      function renderPredictionOutput(lang = getCurrentLang()) {
        predictionGenerated = true;
        const preset = probabilityPresetList[currentPresetIndex];

        // 根据当前模板(A/B) + 当前语言，设置不同的副标题
        if (predictionSubtitle) {
          const subtitles = predictionSubtitleMap[lang] || predictionSubtitleMap['zh'];
          predictionSubtitle.textContent = subtitles[currentPresetIndex] || subtitles[0];
        }

        // 概率数值
        probabilityBadges.forEach(badge => {
          const key = badge.dataset.probKey;
          const value = preset[key] || '--';
          badge.textContent = value;
          badge.classList.remove('opacity-30');
        });

        // 报告内容
        reportContent.classList.remove('text-neutral-400');
        reportContent.classList.add('text-neutral-700');

        if (lang === 'zh') {
          reportContent.innerHTML = reportTemplateZhList[currentPresetIndex];
        } else {
          reportContent.innerHTML = reportTemplateEnList[currentPresetIndex];
        }

          // 🔹 新增：根据当前模板同步更新弹窗图片
          updateModalImages();
      }

      setPredictButtonState(false);
      resetPredictionOutput(getCurrentLang());

      function clampValue(value, min, max) {
        return Math.min(Math.max(Math.round(value), min), max);
      }

      function triggerSlider(slider, value) {
        if (!slider) return;
        slider.value = value;
        slider.dispatchEvent(new Event('input', { bubbles: true }));
      }

      // 设置滑块左侧蓝色渐变
      function setSliderFill(slider) {
        if (!slider) return;
        const min = slider.min ? Number(slider.min) : 0;
        const max = slider.max ? Number(slider.max) : 100;
        const val = Number(slider.value);
        const percent = ((val - min) * 100) / (max - min || 1);
        slider.style.background =
          `linear-gradient(to right, #1E88E5 0%, #1E88E5 ${percent}%, ` +
          `#CBD2D9 ${percent}%, #CBD2D9 100%)`;
      }

      // 自适应亮度 / 对比度计算
      function computeAutoAdjust(imageEl) {
        const fallback = { brightness: 120, contrast: 115 };
        if (!imageEl) return fallback;
        const width = imageEl.naturalWidth || imageEl.width;
        const height = imageEl.naturalHeight || imageEl.height;
        if (!width || !height) return fallback;

        const canvas = document.createElement('canvas');
        const ctx = canvas.getContext('2d', { willReadFrequently: true });
        const target = 256;
        const scale = Math.min(1, target / Math.max(width, height));
        canvas.width = Math.max(1, Math.floor(width * scale));
        canvas.height = Math.max(1, Math.floor(height * scale));
        ctx.drawImage(imageEl, 0, 0, canvas.width, canvas.height);
        const { data } = ctx.getImageData(0, 0, canvas.width, canvas.height);
        const pixels = data.length / 4;
        if (!pixels) return fallback;

        let sum = 0;
        let sumSq = 0;
        for (let i = 0; i < data.length; i += 4) {
          const brightness = 0.299 * data[i] + 0.587 * data[i + 1] + 0.114 * data[i + 2];
          sum += brightness;
          sumSq += brightness * brightness;
        }
        const mean = sum / pixels;
        const variance = Math.max(sumSq / pixels - mean * mean, 0);
        const stdDev = Math.sqrt(variance);
        const targetBrightness = clampValue(100 + (128 - mean) / 1.28, 40, 170);
        const targetContrast = clampValue(100 + (64 - stdDev) / 0.64, 40, 190);
        return { brightness: targetBrightness, contrast: targetContrast };
      }

      /************ 自适应按钮 ************/

      autoSwitches.forEach(btn => {
        btn.addEventListener('click', () => {
          const eye = btn.dataset.autoSwitch;
          const config = sliderMap[eye];
          if (!config) return;

          const isActive = btn.classList.toggle('auto-switch-on');
          btn.setAttribute('aria-pressed', isActive ? 'true' : 'false');

          if (!isActive) {
            // 关闭 -> 恢复默认 100/100
            triggerSlider(config.brightness, 100);
            triggerSlider(config.contrast, 100);
            return;
          }

          // 开启 -> 对当前图像做自动调整
          const srcImg = config.image.__originalImage || config.image;
          const { brightness, contrast } = computeAutoAdjust(srcImg);
          triggerSlider(config.brightness, brightness);
          triggerSlider(config.contrast, contrast);
        });
      });

      /************ 图像上传（计数 + 重置） ************/

      function handleImageUpload(uploadEl, imageEl, previewEl) {
        const placeholder = previewEl.querySelector('.preview-placeholder');
        uploadEl.addEventListener('change', function (e) {
          const file = e.target.files[0];
          if (file) {
            setPredictButtonState(false);
            resetPredictionOutput(getCurrentLang());
            imageEl.dataset.loaded = 'false';

            const reader = new FileReader();
            reader.onload = function (event) {
              const eye = imageEl.id.startsWith('left') ? 'left' : 'right';

              // 关闭自适应开关
              const autoBtn = document.querySelector('[data-auto-switch="' + eye + '"]');
              if (autoBtn) {
                autoBtn.classList.remove('auto-switch-on');
                autoBtn.setAttribute('aria-pressed', 'false');
              }

              // 滑块恢复默认
              const bSlider = document.getElementById(eye + '-brightness');
              const cSlider = document.getElementById(eye + '-contrast');
              const bValue = document.getElementById(eye + '-brightness-value');
              const cValue = document.getElementById(eye + '-contrast-value');
              if (bSlider) { bSlider.value = 100; setSliderFill(bSlider); }
              if (cSlider) { cSlider.value = 100; setSliderFill(cSlider); }
              if (bValue) bValue.textContent = '100';
              if (cValue) cValue.textContent = '100';

              imageEl.dataset.fromUpload = 'true';
              imageEl.src = event.target.result;
              imageEl.classList.remove('hidden');
              if (placeholder) placeholder.classList.add('hidden');
              imageEl.dataset.loaded = 'true';

              // 统计上传次数（用于配对版本切换）
              if (eye === 'left') {
                leftUploadCount++;
              } else {
                rightUploadCount++;
              }
              pairVersion = Math.min(leftUploadCount, rightUploadCount);

              if (leftImage.dataset.loaded === 'true' && rightImage.dataset.loaded === 'true') {
                setPredictButtonState(true);
              }
            };
            reader.readAsDataURL(file);
          } else {
            // 清空文件
            imageEl.dataset.loaded = 'false';
            imageEl.dataset.fromUpload = 'false';

            const eye = imageEl.id.startsWith('left') ? 'left' : 'right';
            const autoBtn = document.querySelector('[data-auto-switch="' + eye + '"]');
            if (autoBtn) {
              autoBtn.classList.remove('auto-switch-on');
              autoBtn.setAttribute('aria-pressed', 'false');
            }
            const bSlider = document.getElementById(eye + '-brightness');
            const cSlider = document.getElementById(eye + '-contrast');
            const bValue = document.getElementById(eye + '-brightness-value');
            const cValue = document.getElementById(eye + '-contrast-value');
            if (bSlider) { bSlider.value = 100; setSliderFill(bSlider); }
            if (cSlider) { cSlider.value = 100; setSliderFill(cSlider); }
            if (bValue) bValue.textContent = '100';
            if (cValue) cValue.textContent = '100';

            setPredictButtonState(false);
            resetPredictionOutput(getCurrentLang());
          }
        });
      }

      handleImageUpload(leftUpload, leftImage, leftPreview);
      handleImageUpload(rightUpload, rightImage, rightPreview);

      /************ 每只眼睛独立处理管线 ************/

      function setupEyeProcessing(prefix) {
        const brightnessSlider = document.getElementById(prefix + '-brightness');
        const brightnessValue = document.getElementById(prefix + '-brightness-value');
        const contrastSlider = document.getElementById(prefix + '-contrast');
        const contrastValue = document.getElementById(prefix + '-contrast-value');
        const image = document.getElementById(prefix + '-image');

        let canvas = document.createElement('canvas');
        let ctx = canvas.getContext('2d');
        let originalImage = null;

        image.addEventListener('load', function () {
          if (image.dataset.fromUpload === 'true') {
            originalImage = new Image();
            originalImage.src = image.src;
            image.__originalImage = originalImage;

            const w = image.naturalWidth || image.width || 1;
            const h = image.naturalHeight || image.height || 1;
            canvas.width = w;
            canvas.height = h;

            image.dataset.fromUpload = 'false';
            applyFilters();
          }
        });

        function applyFilters() {
          if (!originalImage) return;

          const brightness = parseInt(brightnessSlider.value, 10);
          const contrast = parseInt(contrastSlider.value, 10);

          brightnessValue.textContent = brightness;
          contrastValue.textContent = contrast;

          setSliderFill(brightnessSlider);
          setSliderFill(contrastSlider);

          ctx.clearRect(0, 0, canvas.width, canvas.height);
          ctx.filter = `brightness(${brightness}%) contrast(${contrast}%)`;
          ctx.drawImage(originalImage, 0, 0, canvas.width, canvas.height);
          image.src = canvas.toDataURL('image/png');
        }

        brightnessSlider.addEventListener('input', applyFilters);
        contrastSlider.addEventListener('input', applyFilters);

        setSliderFill(brightnessSlider);
        setSliderFill(contrastSlider);
      }

      setupEyeProcessing('left');
      setupEyeProcessing('right');

      // 初始化所有 range 的渐变填充
      document.querySelectorAll('input[type="range"]').forEach(s => {
        setSliderFill(s);
        s.addEventListener('input', () => setSliderFill(s));
      });

      /************ 一键预测按钮 ************/

      predictBtn.addEventListener('click', function () {
        // 判断是否是新的双眼配对
        if (pairVersion !== lastPredictedPairVersion) {
          if (lastPredictedPairVersion !== -1) {
            // 已经预测过，再遇到新配对 -> A/B 之间切换
            currentPresetIndex = 1 - currentPresetIndex;
          }
          lastPredictedPairVersion = pairVersion;
        }

        setPredictButtonState(false);
        this.innerHTML = '<i class="fa fa-spinner fa-spin mr-2"></i>' +
          (document.documentElement.lang === 'zh' ? '预测中...' : 'Predicting...');

        setTimeout(() => {
          const lang = document.documentElement.lang;
          renderPredictionOutput(lang);

          // 预测结果和报告渲染完毕后，弹出图片
          openResultModal();

          this.innerHTML = '<i class="fa fa-stethoscope mr-2"></i>' +
            (lang === 'zh' ? '一键预测' : 'One-Click Predict');
          setPredictButtonState(true);

          reportContent.classList.add('animate-pulse');
          setTimeout(() => {
            reportContent.classList.remove('animate-pulse');
          }, 1000);
        }, 2000);
      });
    });
  </script>
</body>
</html>
