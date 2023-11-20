# 等級誤差についての補足

`photometry.pdf` において、開口測光で求めた測光値の誤差を以下の式で与えた(ただし第１項の２乗は修正済み)  

$$
\sigma_{src}^2 = \left(\frac{1}{g}\sqrt{gF_{src}}\right)^2 +N_{apr}\sigma_{bkg}^2
$$

ここでは、誤差の寄与として  
- 星の光子数の統計的ゆらぎ
- 開口円内の背景光の統計的ゆらぎ

のみを考慮しており具体的には $\sigma_{tot}$ と書くべきである。    
誤差伝搬の式に従うと

$$
F_{src} = F_{tot} - f_{bkg}*N_{apr}
$$

であったので  

$$
\sigma_{src}^2 = \sigma_{tot}^2 +N_{apr}^2 \sigma_{bkg}^2
$$

となるべきである。  

$\sigma_{bkg}$と $\\sigma'_{bkg}$ と区別していることに注目する。  

つまり、ここで $\sigma_{bkg}$ は1画素あたりの背景光の揺らぎを表している。  

一方 $\sigma'_{bkg}$ は円環から測光された背景光の揺らぎを意味する。  

円環の画素数を $N_B$ で表し、各画素についての誤差は等しく $\sigma_{bkg}$ とすれば  

$$
\sigma'_{bkg} = \frac{1}{N_B}\sigma_{bkg}
$$

したがって $F_{src}$ の正しい誤差の式は   

$$
\sigma_{src}^2 = \left(\frac{1}{g}\sqrt{gF_{src}}\right)^2 +N_{apr}\sigma_{bkg}^2 + \frac{N_{apr}^2}{N_B}\sigma_{bkg}^2 
$$
