import os
import time
import requests

# 1. إدخال مفتاح الـ API الخاص بك من منصة Replicate
REPLICATE_API_TOKEN = "your_replicate_api_key_here"

def generate_ai_video(prompt_text):
    headers = {
        "Authorization": f"Token {REPLICATE_API_TOKEN}",
        "Content-Type": "application/json",
    }

    # 2. إرسال أمر توليد الفيديو للنموذج الذكي
    payload = {
        "version": "a4269d5639f3d9b83611d5cf7242d5e71bc20165c84d720b080f33d7b889e472",  # نموذج توليد فيديو
        "input": {
            "prompt": prompt_text,
            "num_frames": 24,
            "fps": 8
        }
    }

    print("جاري إرسال طلب توليد الفيديو...")
    response = requests.post("https://api.replicate.com/v1/predictions", json=payload, headers=headers)
    prediction = response.json()
    
    # 3. الانتظار حتى يكتمل معالجة الفيديو
    prediction_url = prediction["urls"]["get"]
    while prediction["status"] not in ["succeeded", "failed"]:
        print("الذكاء الاصطناعي يقوم بصناعة الفيديو الآن... انتظر بضع ثوانٍ.")
        time.sleep(5)
        prediction = requests.get(prediction_url, headers=headers).json()

    if prediction["status"] == "succeeded":
        video_url = prediction["output"]
        print(f"✅ تم توليد الفيديو بنجاح! رابط التحميل: {video_url}")
        return video_url
    else:
        print("❌ حدث خطأ أثناء توليد الفيديو.")
        return None

# تجربة الكود بوصف إعلان منتج
prompt = "Cinematic slow motion shot of a luxury perfume bottle surrounded by rose petals and smoke, 4k resolution, photorealistic"
generate_ai_video(prompt)
