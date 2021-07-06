# TIL

### 오늘 한 일 
포토폴리오 하나 만들기

### 오늘 배운 일

1. 마커 크기 조절
 plt.figure(figsize=(15,6))

sns.lineplot(data=df, x="Month", y="PercentOfBaseline", hue="Country", marker='o', ci=None)
plt.legend(bbox_to_anchor=(1.02, 1), loc='upper left', borderaxespad=0)
paper_rc = {'lines.linewidth': 1, 'lines.markersize': 5}                  
sns.set_context("paper", rc = paper_rc)
