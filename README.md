# Chinese Character Similarity
A tool for calculating the similarity of two chars.

## Key Idea

### Tone Similarity:

- PinYin edit distance

### Shape Similarity:

- Stroke counts difference
- Sijiao Encoding edit distance
- Character images differences ratio

## CharSimilarity.similarity(ch1, ch2) Usage

Parameters:

- tone:
  - Flag for tone similarity computing. (default: True)
  - Type: Bool
- shape:
  - Flag for shape similarity computing. (default: True)
  - Type: Bool
- wpy:
  - Weight of PinYin similarity. (default: 0.4)
  - Type: Float
  - Range: 0.0 - 1.0
- wst:
  - Weight of stroke count similarity. (default: 0.1)
  - Type: Float
  - Range: 0.0 - 1.0
- wsj:
  - Weight of Sijiao encoding similarity. (default: 0.3)
  - Type: Float
  - Range: 0.0 - 1.0
- wmatrix:
  - Weight of character image matrix similarity. (default: 0.2)
  - Type: Float
  - Range: 0.0 - 1.0
  
```
In [1]: import CharSimilarity

In [2]: ch1 = '侯'

In [3]: ch2 = '候'

In [4]: tone_similarity = CharSimilarity.similarity(ch1,ch2,tone=True,shape=False)

In [5]: print(tone_similarity)
1.0

In [6]: shape_similarity = CharSimilarity.similarity(ch1,ch2,tone=False,shape=True,wpy=0.0,wst=0.33,wsj=0.33,wmatrix=0.34)

In [7]: print(shape_similarity)
0.8253333333333334

In [8]: tone_shape_similarity = CharSimilarity.similarity(ch1,ch2,tone=True,shape=True,wpy=0.4,wst=0.1,wsj=0.3,wmatrix=0.2)

In [9]: print(tone_shape_similarity)
0.9066666666666667
```
## References

- pypinyin Document: http://pypinyin.readthedocs.io/zh_CN/master/index.html
- Pillow Document: https://pillow.readthedocs.io/en/5.1.x/
- 基于音形码的中文字符串相似度算法 - 数据中国: https://blog.csdn.net/chndata/article/details/41114771
- SimilarCharactor - contrl4: https://github.com/contr4l/SimilarCharactor
- 使用Python脚本将文字转换为图片的实例分享 - 老杰: http://www.jb51.net/article/71708.htm
