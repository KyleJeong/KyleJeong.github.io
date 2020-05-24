# KyleJeong.github.io

# Hangul, Hanja
~~~ python
    non_hanja = re.compile(r'[^\u2E80-\u2EFF\u3400-\u4DBF\u4E00-\u9FBF\uF900-\uFAFF\u20000-\u2A6DF\u2F800-\u2FA1F]+')

    # 괄호에 싸인 한자
    hanja     = re.compile(r'\([\u2E80-\u2EFF\u3400-\u4DBF\u4E00-\u9FBF\uF900-\uFAFF\u20000-\u2A6DF\u2F800-\u2FA1F]+\)')

    # 참고자료들
    #      http://jokergt.tistory.com/52 [Gun's Knowledge Base]
    #      https://frody.tistory.com/84 [Frody's]
    #      https://ko.wikipedia.org/wiki/%ED%95%9C%EC%A4%91%EC%9D%BC_%ED%95%9C%EC%9E%90_%ED%9A%8D
    #      https://ko.wikipedia.org/wiki/%EC%9C%A0%EB%8B%88%EC%BD%94%EB%93%9C_%EC%98%81%EC%97%AD
    # 한글
    # preg_match_all('!['
    #     .'\x{1100}-\x{11FF}\x{3130}-\x{318F}\x{AC00}-\x{D7AF}' // Hangul Jamo, // Hangul Compatibility Jamo, // Hangul Syllables (한글 글자마디)
    #     .']+!u', $content, $match);
    # Not listed above
    # U+A960..U+A97F  Hangul Jamo Extended-A
    # U+D7B0..U+D7FF  Hangul Jamo Extended-B

    # 한자
    # preg_match_all('!['
    #     .'\x{2E80}-\x{2EFF}'// 한,중,일 부수 보충 CJK Radicals Supplement
    #     .'\x{31C0}-\x{31EF}\x{3200}-\x{32FF}' // 한중일 한자 획 // 한중일 괄호 문자
    #     .'\x{3400}-\x{4DBF}\x{4E00}-\x{9FBF}\x{F900}-\x{FAFF}' //한중일 통합 한자 확장 A //한중일 통합 한자 // 한중일 호환용 한자, CJK Compatibility Ideographs
    #     .'\x{20000}-\x{2A6DF}\x{2F800}-\x{2FA1F}'// 한,중,일 통합호환한자 B // 한중일 호환용 한자 보충
    #     .']+!u', $content, $match);
    # not listed above
    # U+2F00..U+2FDF  Kangxi Radicals
    # U+2A700..U+2B73F    CJK Unified Ideographs Extension C (한중일 통합 한자 확장 C)
    # U+2B740..U+2B81F    CJK Unified Ideographs Extension D (한중일 통합 한자 확장 D)
    # U+2B820..U+2CEAF    CJK Unified Ideographs Extension E (한중일 통합 한자 확장 E)
    # U+2CEB0..U+2EBEF    CJK Unified Ideographs Extension F (한중일 통합 한자 확장 F)
~~~
