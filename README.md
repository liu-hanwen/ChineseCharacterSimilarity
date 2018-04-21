# SimilarChars
A tool for calculating the similarity of two chars.

## Key Idea

1. Compare the image of characters.
2. How many features matehced will be the similarity of them.

## Workflow

1. Chars --PIL--> Images
2. Images --ORB (Oriented FAST and Rotated BRIEF)--> Two Groups of Features
3. Two Groups of Features --Features Matching--> Similarity

## References

- Feature Detection and Description - OpenCV Python Tutorial: https://docs.opencv.org/3.1.0/db/d27/tutorial_py_table_of_contents_feature2d.html
- 使用Python脚本将文字转换为图片的实例分享 - 老杰: http://www.jb51.net/article/71708.htm
