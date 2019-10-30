# analiseDados



df2 = df[df['TAXA_PARTICIPACAO_5EF'] != 0]


df2['MEDIA_5EF_LP'].quantile(q=0.25)
df2['MEDIA_5EF_LP'].quantile(q=0.5)
df2['MEDIA_5EF_LP'].quantile(q=0.75)



df1Q = df2[df2['MEDIA_5EF_LP']<=186.28]
f4Q = df2[df2['MEDIA_5EF_LP']>=224.07]

df1Q['ROTULO'] = 0
df4Q['ROTULO'] = 1


treino_base_LP = pd.concat([df4Q , df1Q])
