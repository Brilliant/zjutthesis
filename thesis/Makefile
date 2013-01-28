#
# build zjutmain.pdf
#

# XXX: bibtex 会报错 如 http://bbs.sjtu.edu.cn/bbstcon,board,TeX_LaTeX,reid,1299228706.html 
# 原因是bibtex处理中文字符的能力(无论是GBK还是UTF-8)都有点点问题，
# 正常是用也是会出现这些提示的。
# 不影响结果输出，这里ignore掉。
.IGNORE : all 

all:
	xelatex zjutmain
	bibtex zjutmain
	xelatex zjutmain
	xelatex zjutmain

clean:
	git clean -fx

png:
	mkdir -p preview; cp zjutmain.pdf preview/; cd preview; rm *.png; pdftoppm -png zjutmain.pdf zjutmain_preview; rm -rf zjutmain.pdf; cd ..
