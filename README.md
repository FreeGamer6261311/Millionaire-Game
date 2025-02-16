										Rahman ve Rahim olan Allah'ın adıyla;
									Kovulmuş şeytanın şerrinden Allah'a sığınırım.

						-Kim Milyoner Olmak İster HTML5 Yazılım Tabanlı Oyun Kullanım Kılavuzu-

Kullanım
Bu oyunu "kurmak" için statik dosyaları sunabilen basit bir web sunucusuna ihtiyacınız var (Apache gibi). Git deposunu bir web sunucusundaki bir klasöre yükleyin ve tarayıcınızda index.html dosyasını açın.

Scraping / Soru Bankası
Soruları toplama sürecini kolaylaştırmak için /util klasörüne indiabix.com sitesinden soru çeken bir Python betiği ekledim.

Kök dizinde questions.json ana soru dosyası olarak bulunur. Ayrıca questions2.json adlı başka bir soru seti daha mevcuttur, ancak program yalnızca questions.json dosyasını okur.

Soru Formatı
Soru bankası, "oyunlar" dizisi içeren bir JSON dosyasıdır. İstediğiniz kadar oyun ekleyebilirsiniz. Oyunu başlatırken seçim yapabilirsiniz.

json
Kopyala
Düzenle
{
    "games": [
        {
            "questions": [ ... ]
        },
        {
            "questions": [ ... ]
        }, ...
    ]
}
Her bir soru dizisi aşağıdaki formattadır:

"content" anahtarı, 4 çoktan seçmeli cevabı içeren bir dizidir (tam olarak 4 seçenek olmalıdır).
"question" anahtarı, soru metnini içerir.
"correct" anahtarı, "content" dizisindeki doğru cevabın sıfır tabanlı indeksini belirtir.
Örnek:

json
Kopyala
Düzenle
{
    "question": "Aurora Borealis yaygın olarak ne olarak bilinir?",
    "content": [
        "Peri Tozu",
        "Kuzey Işıkları",
        "Çağlar Kitabı",
        "Game of Thrones ana karakteri"
    ],
    "correct": 1
}
Bu örnekte, doğru cevap "Kuzey Işıkları" olduğu için "correct": 1 olarak belirtilmiştir.

İyi kullanımlar dileği ile.

                                                                                            Mustafa Yazıcı