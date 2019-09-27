# Multi Byte Komutları (Çok baytlı Dizge İşlevleri)

Türkçe karakterde sorun çıkarabilmektedir. Bunun olmaması için ```php.ini``` dosyasında mbstring.language değişkenin değerinin Turkish olarak ayarlanması gerekmektedir.


```ini_set('mbstring.language','Turkish');```

## Komut Listesi

Komut |Anlamı|
------------|-------------|
[mb_check_encoding](http://php.net/mb-check-encoding) |Dizgenin belirtilen kodlama için geçerli olup olmadığını sınar
[mb_chr](http://php.net/mb-chr)| Get a specific character
[mb_convert_case](http://php.net/mb-convert-case)| Bir dizgeye büyük-küçük harf dönüşümü uygular
[mb_convert_encoding](http://php.net/mb-convert-encoding) |Karakter kodlaması dönüşümü yapar
[mb_convert_kana](http://php.net/mb-convert-kana)| Bir "kana" dizgeyi diğerine ("zen-kaku", "han-kaku" vs.) dönüştürür
[mb_convert_variables](http://php.net/mb-convert-variables)| Değişken içeriğinin karakter kodlamasını dönüştürür
[mb_decode_mimeheader](http://php.net/mb-decode-mimeheader)| MIME başlık alanındaki dizgeyi dönüştürür
[mb_decode_numericentity](http://php.net/mb-decode-numericentity)| HTML sayısal karakter gösterimini karaktere dönüştürür
[mb_detect_encoding](http://php.net/mb-detect-encoding)| Karakter kodlamasını algılar
[mb_detect_order](http://php.net/mb-detect-order)| Karakter kodlaması algılama sırasını tanımlar/döndürür
[mb_encode_mimeheader](http://php.net/mb-encode-mimeheader)| Dizgeyi MIME başlığı için kodlar
[mb_encode_numericentity](http://php.net/mb-encode-numericentity)| Karakter kodlarını HTML sayısal karakter gösterimlerine dönüştürür
[mb_encoding_aliases](http://php.net/mb-encoding-aliases)| Get aliases of a known encoding type
[mb_ereg_match](http://php.net/mb-ereg-match) |Çok baytlı dizge için düzenli ifadeyi eşleştirir
[mb_ereg_replace_callback](http://php.net/mb-ereg-replace-callback)| Perform a regular expresssion seach and replace with multibyte support using a callback
[mb_ereg_replace](http://php.net/mb-ereg-replace)| Çok baytlı karakter destekli düzenli ifade yer değiştirmesi yapar
[mb_ereg_search_getpos](http://php.net/mb-ereg-search-getpos)| Sonraki düzenli ifade eşleşmesi için başlangıç konumunu döndürür
[mb_ereg_search_getregs](http://php.net/mb-ereg-search-getregs)| Sonuncu çok baytlı düzenli ifade eşleşmesinin sonucunu döndürür
[mb_ereg_search_init](http://php.net/mb-ereg-search-init)| Çok baytlı düzenli ifade eşleşmesi için kullanılacak dizge ve düzenli ifadeyi tanımlar
[mb_ereg_search_pos](http://php.net/mb-ereg-search-pos)| Evvelce tanımlanmış çok baytlı dizge için çok baytlı düzenli ifadenin eşleşen parçasının uzunluğunu ve konumunu döndürür
[mb_ereg_search_regs](http://php.net/mb-ereg-search-regs)| Çok baytlı düzenli ifadenin eşleşen parçası ile döner
[mb_ereg_search_setpos](http://php.net/mb-ereg-search-setpos)| Sonraki düzenli ifade eşleşmesinin başlangıç noktasını tanımlar
[mb_ereg_search](http://php.net/mb-ereg-search)| Evvelce tanımlanmış çok baytlı dizge için çok baytlı düzenli ifade eşleştirmesi yapar
[mb_ereg](http://php.net/mb-ereg)| Düzenli ifadeyi çok baytlı karakter desteğiyle eşleştirir
[mb_eregi_replace](http://php.net/mb-eregi-replace)| Harf büyüklüğüne duyarsız çok baytlı karakter destekli düzenli ifade yer değiştirmesi yapar
[mb_eregi](http://php.net/mb-eregi)| Harf büyüklüğüne duyarsız çok baytlı düzenli ifade eşleştirmesi uygular
[mb_get_info](http://php.net/mb-get-info)| Mbstring değiştirgelerinin dahili ayarlarını döndürür
[mb_http_input](http://php.net/mb-http-input)| HTTP girdi karakter kodlamasını algılar
[mb_http_output](http://php.net/mb-http-output)| HTTP çıktı karakter kodlamasını tanımlar/döndürür
[mb_internal_encoding](http://php.net/mb-internal-encoding)| Dahili karakter kodlamasını tanımlar/döndürür
[mb_language](http://php.net/mb-language)| Geçerli dili tanımlar/döndürür
[mb_list_encodings](http://php.net/mb-list-encodings)| Desteklenen kodlamaların tamamını bir dizi olarak döndürür
[mb_ord](http://php.net/mb-ord)| Get code point of character
[mb_output_handler](http://php.net/mb-output-handler)| Çıktı tamporundaki karakter kodlamasını dönüştüren geriçağırım işlevi
[mb_parse_str](http://php.net/mb-parse-str)| GET/POST/COOKIE verisini çözümler ve küresel değişkenleri tanımlar
[mb_preferred_mime_name](http://php.net/mb-preferred-mime-name)| MIME karakter kümesi dizgesini döndürür
[mb_regex_encoding](http://php.net/mb-regex-encoding)| mbregex işlevleri için geçerli kodlamayı dizge olarak döndürür
[mb_regex_set_options](http://php.net/mb-regex-set-options)| mbregex işlevleri için öntanımlı seçenekleri tanımlar/döndürür
[mb_scrub](http://php.net/mb-scrub)| Description
[mb_send_mail](http://php.net/mb-send-mail)| Kodlanmış olarak posta gönderir
[mb_split](http://php.net/mb-split)| Çok baytlı bir dizgeyi düzenli ifade ile parçalara ayırır
[mb_strcut](http://php.net/mb-strcut)| Dizgenin başlangıcı ve uzunluğu belirtilen parçası ile döner
[mb_strimwidth](http://php.net/mb-strimwidth)| Dizgeyi belirtilen genişlikte kırpar
[mb_stripos](http://php.net/mb-stripos)| Harf büyüklüğüne duyarsız olarak, bir dizgenin içinde başka bir dizgeye ilk rastlanılan noktanın indisini döndürür
[mb_stristr](http://php.net/mb-stristr)| Harf büyüklüğüne duyarsız olarak, bir dizgenin içinde başka bir dizgeye ilk rastlanılan noktaya göre dizgenin ilk veya son bölümü ile döner
[mb_strlen](http://php.net/mb-strlen)| Dizge uzunluğu ile döner
[mb_strpos](http://php.net/mb-strpos) |Bir dizgenin içinde başka bir dizgeye ilk rastlanılan noktanın indisini döndürür
[mb_strrchr](http://php.net/mb-strrchr)| Bir dizgenin içinde bulunan bir karaktere göre dizgenin ilk veya son bölümü ile döner
[mb_strrichr](http://php.net/mb-strrichr)| Harf büyüklüğüne duyarsız olarak bir dizgenin içinde bulunan bir karaktere göre dizgenin ilk veya son bölümü ile döner
[mb_strripos](http://php.net/mb-strripos)| Bir dizgenin içinde harf büyüklüğüne duyarsız olarak başka bir dizgeye son rastlanılan noktanın indisini döndürür
[mb_strrpos](http://php.net/mb-strrpos)| Bir dizgenin içinde başka bir dizgeye son rastlanılan noktanın indisini döndürür
[mb_strstr](http://php.net/mb-strstr)| Bir dizgenin içinde başka bir dizgeye ilk rastlanılan noktaya göre dizgenin ilk veya son bölümü ile döner
[mb_strtolower](http://php.net/mb-strtolower)| Dizgeyi küçük harfli yapar
[mb_strtoupper](http://php.net/mb-strtoupper)| Dizgeyi büyük harfli yapar
[mb_strwidth](http://php.net/mb-strwidth)| Dizge genişliğini döndürür
[mb_substitute_character](http://php.net/mb-substitute-character)| İkame karakteri atar/döndürür
[mb_substr_count](http://php.net/mb-substr-count)| Mevcut alt dizgelerin sayısı ile döner
[mb_substr](http://php.net/mb-substr)| Dizgenin bir alt dizgesini alır
