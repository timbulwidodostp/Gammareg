# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Classic gamma regression models Use Gammareg With (In) R Software
install.packages("Gammareg")
library("Gammareg")
Gammareg = read.csv("https://raw.githubusercontent.com/timbulwidodostp/Gammareg/main/Gammareg/Gammareg.csv",sep = ";")
# Estimation Classic gamma regression models Use Gammareg With (In) R Software
X1_log <- cbind(Gammareg$X1_log)
X2_log <- cbind(Gammareg$X2_log)
X3_log <- cbind(Gammareg$X3_log)
X4_log <- cbind(Gammareg$X4_log)
Y_log <- cbind(Gammareg$Y_log)
Z_log <- cbind(X1_log, X2_log, X4_log)
formula.mean = Y_log ~ X2_log + X3_log
formula.shape = ~ X2_log + X4_log
gammareg_log=Gammareg(formula.mean, formula.shape, meanlink="log")
summary(gammareg_log)
X1_ide <- cbind(Gammareg$X1_ide)
X2_ide <- cbind(Gammareg$X2_ide)
X3_ide <- cbind(Gammareg$X3_ide)
X4_ide <- cbind(Gammareg$X4_ide)
Y_ide <- cbind(Gammareg$Y_ide)
Z_ide <- cbind(X1_ide, X2_ide, X4_ide)
formula.mean = Y_ide ~ X2_ide + X3_ide
formula.shape = ~ X2_ide + X4_ide
gammareg_ide=Gammareg(formula.mean, formula.shape, meanlink="ide")
summary(gammareg_ide)
# Classic gamma regression models Use Gammareg With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished