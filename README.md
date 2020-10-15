import math 
import numpy as np 
import matplotlib.pyplot as plt 
import mpl_toolkits.axisartist as axisartist 
plt.rcParams['font.sans-serif']=['SimHei']
plt.rcParams['axes.unicode_minus']=False

fig=plt.figure(figsize=(6,4)) 
ax=axisartist.Subplot(fig,111) 
fig.add_axes(ax) 

def exponential_func(x, a=1.5):
  y=math.pow(a, x)
  return y

X=np.linspace(-4, 4, 40) 
Y=[exponential_func(x) for x in X]
ax.plot(X, Y) 
def exponential_func(x, a=0.67): 
  y=math.pow(a, x)
  return y

a=np.arange(-2*np.pi,2*np.pi,0.01)
b=np.sin(a)
plt.plot(a,b)

X=np.linspace(-4, 4, 40) 
Y=[exponential_func(x) for x in X] 
ax.plot(X, Y) 
ax.axis[:].set_visible(False)
ax.axis["x"]=ax.new_floating_axis(0, 0, axis_direction="bottom") 
ax.axis["y"]=ax.new_floating_axis(1, 0, axis_direction="bottom") 
ax.axis["x"]=ax.new_floating_axis(0, 0, axis_direction="bottom") 
ax.axis["y"]=ax.new_floating_axis(1, 0, axis_direction="bottom") 

ax.axis["x"].set_axisline_style("-|>", size=1.0) 
ax.axis["y"].set_axisline_style("-|>", size=1.0) 
ax.annotate(s='x', xy=(max(X), 0), xytext=(max(X)+0.5, 0.5)) 
ax.annotate(s='y', xy=(0, 1.0), xytext=(-0.5, max(Y)+0.5)) 
plt.xticks([-np.pi*2,-np.pi*3/2,-np.pi, -np.pi/2, 0, np.pi/2, np.pi,np.pi*3/2,np.pi*2],[r'$-2\pi$',r'$-\frac{3}{2} \pi$',r'$-\pi$',r'$-\frac{1}{2}\pi$', r'0', r'$\frac{1}{2}\pi$','$\pi$',r'$\frac{3}{2}\pi$',r'$2 \pi$'])
plt.ylim((-1, 1))
plt.show()

