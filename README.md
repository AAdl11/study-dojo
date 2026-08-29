# Study Dojo

Self-quizzing rooms for my coursework at Las Positas College.
Built for fast review before class Kahoots and Canvas quizzes.

## ▶️ Play Now

| Room | Course | Status |
|---|---|---|
| **[comm-l1](https://aadl11.github.io/study-dojo/dojo/comm-l1/)** | COMM L1 · Public Speaking | ✅ Ch 9–11 · 87 questions |
| [psyc4](https://aadl11.github.io/study-dojo/) | PSYC 4 · Module 0 (legacy path) | 🔜 moving into `dojo/psyc4/` |
| psyc21 | PSYC 21 · Race & Identity | Setting up |
| psyc-c1000 | PSYC C1000 · Summer foundations | Setting up |
| eng7 | ENG 7 · Summer English | Setting up |

→ [All rooms](https://aadl11.github.io/study-dojo/dojo/)

Opens in any browser, phone or laptop. On mobile, use **Add to Home Screen** — it behaves like an app, nothing to download.

## What's in each room

Key-concept map · vocabulary with audio · flashcards · timed self-quiz with a wrong-answer bank · Jeopardy-style rapid-fire board.

## Structure

```
dojo/
  index.html      hub
  comm-l1/
    index.html    one self-contained file per course
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
