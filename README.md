# Study Dojo

Self-quizzing rooms for my coursework at Las Positas College.
Built for fast review before class Kahoots and Canvas quizzes.

## ▶️ Play Now

| Room | Course | Status |
|---|---|---|
| **[psyc4](https://aadl11.github.io/study-dojo/dojo/psyc4/)** | PSYC 4 · Brain, Mind & Behavior | ✅ Module 0 · 47 terms · 20 questions ｜ [Ch 2](https://aadl11.github.io/study-dojo/psyc4-ch2.html) · [Ch 3](https://aadl11.github.io/study-dojo/psyc4-ch3.html) · [Ch 3 Kahoot 40](https://aadl11.github.io/study-dojo/PSYC4_Ch3_Kahoot_40.html) |
| **[psyc21](https://aadl11.github.io/study-dojo/dojo/psyc21/)** | PSYC 21 · Race & Identity | ✅ Ch 1 · 44 terms · 30 questions |
| **[comm-l1](https://aadl11.github.io/study-dojo/dojo/comm-l1/)** | COMM L1 · Public Speaking | ✅ Ch 9–11 · 87 questions |
| **[psyc-c1000](https://aadl11.github.io/study-dojo/)** | PSYC C1000 · Summer foundations | ✅ 15 ch · 329 points · 90 questions（舊複習中心） |
| **[eng7](https://aadl11.github.io/study-dojo/)** | ENG 7 · Summer English | ✅ 批判文・政策主張 兩個道場（舊複習中心） |

→ [All rooms](https://aadl11.github.io/study-dojo/dojo/)

Opens in any browser, phone or laptop. On mobile, use **Add to Home Screen** — it behaves like an app, nothing to download.

## What's in each room

Key-concept map · vocabulary with audio · flashcards · timed self-quiz with a wrong-answer bank · Jeopardy-style rapid-fire board.

## Structure

```
dojo/
  index.html      hub（前門：每門課一顆按鈕）
  psyc4/index.html
  psyc21/index.html
  comm-l1/index.html
index.html        舊複習中心（C1000、ENG 7 的內容還在這裡）
psyc4-ch2.html / psyc4-ch3.html / PSYC4_Ch3_Kahoot_40.html   PSYC 4 早期單檔
```

One folder per course, one `index.html` per room. All content lives in the data arrays inside that file — **add questions by editing the arrays, never the layout**. Rooms are independent: updating one course touches nothing else.

## Question-generation prompt

Reusable for any course. Paste the source material at the end, then merge the output array into that course's room.

```
你是我的考試出題助手。只輸出一個 JavaScript 陣列，不要任何其他文字。
每個元素格式：
{c:單元編號, q:"題目", o:["選項1","選項2","選項3","選項4"], a:正確選項索引(0起算), e:"一句解釋，點出易混淆處"}
依據下面貼的教材出 30 題繁體中文選擇題（專有名詞保留英文），
涵蓋所有粗體術語，其中至少 10 題是情境應用題
（給一個例子，問屬於哪個概念）——這是為了課堂 Kahoot 搶答練反應。
=== 教材開始 ===
[paste syllabus / lecture slides / transcript here]
```
