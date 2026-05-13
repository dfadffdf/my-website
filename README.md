<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI 자소서 마스터</title>
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --accent-purple: #a855f7;
            --accent-cyan: #22d3ee;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --input-bg: #0f172a;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, Roboto, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }

        .container {
            width: 100%;
            max-width: 600px;
            background-color: var(--card-bg);
            padding: 40px;
            border-radius: 24px;
            border: 1px solid rgba(168, 85, 247, 0.3);
            box-shadow: 0 0 40px rgba(168, 85, 247, 0.2);
        }

        h1 {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 10px;
            color: #6366f1; /* 밝은 블루/퍼플 */
        }

        .subtitle {
            text-align: center;
            color: var(--text-muted);
            margin-bottom: 30px;
            font-size: 0.95rem;
        }

        .input-group-row {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
        }

        .input-group-row input {
            flex: 1;
        }

        input[type="text"], textarea {
            width: 100%;
            background-color: var(--input-bg);
            border: 1px solid #334155;
            border-radius: 12px;
            padding: 15px;
            color: white;
            box-sizing: border-box;
            outline: none;
            transition: border-color 0.2s;
        }

        input:focus, textarea:focus {
            border-color: var(--accent-purple);
        }

        textarea {
            resize: vertical;
            min-height: 100px;
        }

        .section-label {
            display: flex;
            justify-content: space-between;
            margin: 20px 0 10px;
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* 슬라이더 스타일링 */
        .slider-container {
            margin-bottom: 20px;
        }

        .slider-label {
            font-size: 0.85rem;
            color: var(--text-muted);
            margin-bottom: 8px;
        }

        input[type="range"] {
            width: 100%;
            height: 6px;
            background: #334155;
            border-radius: 5px;
            outline: none;
            appearance: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            appearance: none;
            width: 18px;
            height: 18px;
            background: var(--accent-cyan);
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 0 10px var(--accent-cyan);
        }

        .char-count {
            margin-top: 10px;
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        /* 버튼 스타일 */
        .button-group {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }

        .btn {
            flex: 1;
            padding: 15px;
            border-radius: 12px;
            border: none;
            font-weight: bold;
            cursor: pointer;
            color: black;
            background: linear-gradient(90deg, #7c3aed, #06b6d4);
            transition: opacity 0.2s;
        }

        .btn:hover {
            opacity: 0.9;
        }

        /* 하단 정보 박스 */
        .info-box {
            margin-top: 30px;
            background-color: rgba(15, 23, 42, 0.5);
            border: 1px solid #334155;
            border-radius: 12px;
            padding: 15px;
            font-size: 0.85rem;
            color: var(--text-muted);
            line-height: 1.6;
        }

        .info-box ul {
            margin: 0;
            padding-left: 20px;
            list-style-type: "- ";
        }
    </style>
</head>
<body>

<div class="container">
    <h1>AI 자소서 마스터</h1>
    <p class="subtitle">AI가 자기소개서를 분석하고 개선점을 제안합니다</p>

    <div class="input-group-row">
        <input type="text" placeholder="기업명">
        <input type="text" placeholder="지원 직무">
    </div>

    <textarea placeholder="직무 설명 (선택사항)" style="margin-bottom: 15px;"></textarea>
    
    <input type="text" placeholder="자기소개서 문항" style="margin-bottom: 20px;">

    <div class="section-label">
        <span>글자수 제한</span>
        <span>0~1000자</span>
    </div>

    <div class="slider-container">
        <div class="slider-label">최소 글자수:</div>
        <input type="range" min="0" max="1000" value="100">
    </div>

    <div class="slider-container">
        <div class="slider-label">최대 글자수:</div>
        <input type="range" min="0" max="1000" value="800">
    </div>

    <textarea placeholder="자기소개서 내용을 입력하세요" style="min-height: 200px;"></textarea>
    <div class="char-count">현재 글자수: 0자</div>

    <div class="button-group">
        <button class="btn">분석하기</button>
        <button class="btn">초기화</button>
    </div>

    <div class="info-box">
        <ul>
            <li>정확한 분석을 위해서는 직무 설명을 입력해주세요.</li>
            <li>분석 결과는 참고용으로만 사용해주세요.</li>
            <li>기존 자소서의 내용을 기반으로 첨삭이 진행됩니다.</li>
        </ul>
    </div>
</div>

</body>
</html>
