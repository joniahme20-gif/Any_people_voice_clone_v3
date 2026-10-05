# 🇧🇩 Any People BD Voice Clone Turbo

উন্নত বাংলা ভয়েস ক্লোনিং — **এক ক্লিকে Google Colab-এ চালান।** ইঞ্জিন: [OmniVoice](https://github.com/k2-fsa/OmniVoice) (৬০০+ ভাষা, বাংলাসহ)।

<p align="center">
  <a href="https://colab.research.google.com/github/YOUR_GITHUB_USERNAME/Any-People-BD-Voice-Clone/blob/main/Any_People_BD_Voice_Clone_Turbo.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
  </a>
</p>

## কীভাবে চালাবেন
1. উপরের **Open In Colab** বাটনে ক্লিক করুন।
2. `Runtime → Change runtime type → T4 GPU`।
3. `Runtime → Run all`।

## ফিচার
- রেফারেন্স অডিও অটো ক্লিন-আপ (নয়েজ রিমুভ, লাউডনেস, সেরা অংশ বাছাই, কোয়ালিটি রিপোর্ট)
- বাংলা Whisper ট্রান্সক্রিপশন
- Best-of-N + ASR যাচাই
- উন্নত বাংলা নরমালাইজার (লাখ/কোটি, ফোন, তারিখ, সময়, টাকা, শতাংশ)
- ⚡ Turbo Engine (ব্যাচিং, স্ট্রিমিং, LRU ক্যাশ)
- ⚡ দ্রুত স্টার্ট: যা নেই শুধু তাই ইনস্টল, `hf_transfer` দিয়ে দ্রুত মডেল ডাউনলোড
- 📊 জেনারেটের সময় লাইভ শতাংশ (Colab বার, Gradio UI, ওয়েব পেজ)
- Google Drive-এ স্থায়ী ভয়েস লাইব্রেরি
- লাইভ URL সার্ভার (FastAPI + Cloudflare) ও `/live` রিয়েল-টাইম পেজ
- ব্যাচ জেনারেশন + ZIP, বাংলা Gradio UI
- LoRA ফাইন-টিউনিং

## ফোল্ডার
| পথ | কী আছে |
|---|---|
| `Any_People_BD_Voice_Clone_Turbo.ipynb` | মূল Colab নোটবুক (সব কোড এর ভেতরেই) |
| `bdvoice/` | নোটবুকের কোড সেল-ভিত্তিক আলাদা ফাইলে (পড়া, ভার্সন, টেস্টের জন্য) |
| `web/index_v2.html` | লাইভ সার্ভারের UI |
| `docs/` | ব্যবহার, আর্কিটেকচার, ফাইন-টিউনিং, টিপস |
| `examples/` | নমুনা টেক্সট |
| `tests/` | নরমালাইজার ও কাঠামো টেস্ট |
| `tools/` | `set_github_user.py`, `sync_from_notebook.py` |

নোটবুক বদলালে `python tools/sync_from_notebook.py` চালালে `bdvoice/` ও `web/` আবার মিলে যায়।

## নিজের GitHub-এ বসানো
```
python tools/set_github_user.py আপনার_ইউজারনেম
```
এটি README-র Colab লিংকে `YOUR_GITHUB_USERNAME` বদলে দেয়। রিপোর নাম `Any-People-BD-Voice-Clone` ও রিপো **Public** রাখুন।

## ⚠️ দায়িত্বশীল ব্যবহার
শুধু নিজের কণ্ঠ বা যার **স্পষ্ট অনুমতি** আছে তার কণ্ঠ ক্লোন করুন। প্রতারণা, ভুয়া খবর বা ছদ্মবেশ ধারণে ব্যবহার নিষিদ্ধ।

## কৃতজ্ঞতা
[OmniVoice](https://github.com/k2-fsa/OmniVoice) (Apache-2.0) — এই রিপোতে এর কোড কপি করা হয়নি, `pip install omnivoice` দিয়ে ইনস্টল হয়।
