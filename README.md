# News-Image-Generator
Generates images based on a paragraph, translates it to English, and feeds it into Stability AI text-to-image API to generate image.
This project includes Stability AI text-to-image API, which is a paid feature.
Since an OpenAI GPT API is also a paid feature, we didn't actually use it. Instead, we manually put the paragraph in the ChatGPT online and get the excerpted sentence, then feed it in the Google translation API . But this can also be done by hooking up to the GPT API so the process could be completely automatic.
## Style
We demanded a consistent style for the news agency, so that the reader could recognize intuitively where the image comes from, and we didn't want to generate a realistic image that may mislead readers into believing that the image is real, so we ended on the 'caricature in lively color' style.
Below are several examples of the original paragraph (in Taiwanese Traditional Chinese), the extracted sentence, the translated sentence (in English), and the final outputted image.
## Examples
### 1. A Storm in Mexico Drives People to Hoard
#### Original Paragraph
  英國遭逢巴貝特風暴的侵襲，當地氣象單位週末前兩度發布紅色警報，各地傳出淹水災情。而巴貝特一路往丹麥和德國前進，強度在20日達到最高峰。中美洲的墨西哥則迎來三級颶風諾瑪，居民湧入超市採買，加油站則出現排隊的車流。(From PTS Taiwan)
#### Excerpted Sentence(s)
  中美洲的墨西哥則迎來三級颶風諾瑪，居民湧入超市採買，加油站則出現排隊的車流。
#### Translation
  Mexico, in Central America, faced Category 3 Hurricane Norma. Residents flocked to supermarkets to buy goods, and there were queues of cars at gas stations.
#### Generated Image
![風暴_full](https://github.com/ssuyung/News-Image-Generator/assets/39045469/8adbc718-d76c-42f7-95e7-9fd4190e1f21)
### 2. Israel-Palestine Conflict
#### Original Paragraph
  《路透社》寫道，沙烏地阿拉伯是中東大國，也是伊斯蘭其中2大聖地麥加與麥地那的所在地。2020年，在川普政府斡旋下，鄰國巴林及阿拉伯聯合大公國與以色列建交，當時利雅德給予祝福但未跟進，宣稱應該首先解決巴勒斯坦的建國目標。(From ETtoday)
#### Excerpted Sentence(s)
  2020年，在川普政府斡旋下，鄰國巴林及阿拉伯聯合大公國與以色列建交。
#### Translation
  In 2020, under the mediation of the Trump administration, neighboring Bahrain and the United Arab Emirates established diplomatic relations with Israel.
#### Generated Image
![以巴_full](https://github.com/ssuyung/News-Image-Generator/assets/39045469/640f7acc-a5a9-4e67-9c45-39ee71fcaee5)

### 3. Successive Power Outage in NTHU
#### Original Paragraph
  清大女同學在Dcard上發文，「清大短短10天停電6次，根本活在難民營」，從9日無預警停電開始，10天內就停電6次，其中有3次是無預警，學生們冰箱食物全壞、各種電器因停電受損甚至直接死機、報告沒存到檔直接飛灰煙滅、工作站死機根本沒辦法寫程式交作業、睡到一半被斷電熱醒。(From ETtoday)
#### Excerpted Sentence(s)
  大學停電，教室漆黑(Tuned Excerpt)
#### Translation
  There is a power outage in the university and the classrooms are dark
#### Generated Image
![教室漆黑3_full](https://github.com/ssuyung/News-Image-Generator/assets/39045469/e24ae527-bbba-4f0e-beb0-3ba6d95ef563)
### 4. Meichu Hackathon 2023
#### Original Paragraph
  2023新竹X梅竹黑客松競賽活動，21日於清華大學體育館盛大開幕，由新竹市政府、台積電等6家企業、清華大學及陽明交大梅竹黑客松籌備團隊共同合作舉辦，今年逾200人參賽，競爭相當激烈。市長高虹安表示，黑客松參賽者來自全國各地的菁英隊伍，希望透過競賽讓青年發揮專業長才、學習團隊合作、激發創意思考以及整合能力，發揮青年的無限創造力，展現亮眼的成果。(From ETaiwan News東台灣新聞網)
#### Excerpted Sentence(s)
  清華大學體育館內，參賽者來自全國各地，圍坐在電腦前，熱烈討論、合作解決問題，場面熱鬧且充滿創意氛圍，各方代表共同見證競賽盛況。(In the prompt we asked to depict an image of the above paragraph)
#### Translation
  In the Tsinghua University Gymnasium, contestants from all over the country sat around the computer, discussing and collaborating to solve problems. The scene was lively and full of creativity, and representatives from all parties witnessed the grand competition.
#### Generated Image
![黑客松_full](https://github.com/ssuyung/News-Image-Generator/assets/39045469/2c6a7cdd-d241-4fb1-9cfd-b8dbf1ea8572)

### 5. A Stupid Fight between Two Diner in a Japanese Restaurant
#### Original Paragraph
  有網友在臉書社團「爆料公社」貼出2段影片，第一段看到刺青男方2男1女與眼鏡男方2男1女在店內隔空互嗆，黑衣刺青男問「你看著我幹嘛？」灰衣眼鏡男則說「有什麼問題啦？我點個茶碗蒸有什麼問題啦？」綠衣刺青男則說：「你點茶碗蒸是你的問題，X你X一直看著我幹嘛？有什麼問題嗎？怎麼了？大哥怎麼了？」此時，灰衣眼鏡男站起來並拿起杯子怒敲了一下桌面說「我點茶碗蒸而已」，結果綠衣刺青男回嗆「你看起來就像茶碗蒸」。 (From ETtoday) 
#### Excerpted Sentence(s)
  灰衣眼鏡男站起來並拿起杯子怒敲了一下桌面
#### Translation
  The man in gray clothes and glasses stood up, picked up the cup and knocked on the table angrily.
#### Generated Image
  ![茶碗蒸_full2](https://github.com/ssuyung/News-Image-Generator/assets/39045469/d92c3f4d-56a0-4a43-98f2-7e2d4e7a6e79)
![灰衣男_full](https://github.com/ssuyung/News-Image-Generator/assets/39045469/d2a11129-1f66-4b2f-9b8d-b6f7123fe991)

