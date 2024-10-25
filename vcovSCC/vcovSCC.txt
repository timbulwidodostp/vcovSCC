# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Regression with Driscoll-Kraay robust standard errors for panels with cross-sectional dependence Use vcovSCC (plm) With R Software
install.packages("plm")
library("plm")
library("lmtest")
vcovSCC = read.csv("https://raw.githubusercontent.com/timbulwidodostp/vcovSCC/main/vcovSCC/vcovSCC.csv",sep = ";")
# Estimation Regression with Driscoll-Kraay robust standard errors for panels with cross-sectional dependence Use vcovSCC (plm) With R Software
# Pooled OLS estimation (Model Common Effect)
Common = plm (invest ~ mvalue + kstock, data = vcovSCC, effect = "twoways",model = "pooling")
Common <- coeftest(Common, vcovSCC(Common))
Common
# Fixed-effects (within) regression (Model Fixed Effect)
Fixed = plm (invest ~ mvalue + kstock, data = vcovSCC, effect = "twoways",model = "within")
Fixed <- coeftest(Fixed, vcovSCC(Fixed))
Fixed
# Regression with Driscoll-Kraay robust standard errors for panels with cross-sectional dependence Use vcovSCC (plm) With R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
