# duilib
- Դ��Դ��googlecode����������googlecode���Ѿ��Ҳ����ˣ�����Ŀǰά����GitHub��Ŀ��[duilib](https://github.com/duilib/duilib)

��ֵ��ǹٷ��汾�����ṩDuiDesigner����UI��ƹ��ߣ�����������ά����һ���汾�������޸���һЩ���⣬���Ż����÷���

�ռ��ĺܶ����duilib������demo�ƶ��������[bigsinger/duilibdemo](https://github.com/bigsinger/duilibdemo)


# ����
## ռλ��
������
```xml
<Control />
```
���ߣ�
```xml
<Container />
```

ˮƽ���֣�HorizontalLayout����**���Ϊ1�ĺ�ɫ�ָ���**��
```xml
<Control width="1" bkcolor="#0" />
```

## ��ֱ������
��<Window>�ӽڵ�����ӣ�
```xml
<Default name="VScrollBar" value="button1normalimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;0,0,16,16&apos;&quot; button1hotimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;16,0,32,16,16&apos;&quot; button1pushedimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;32,0,48,16&apos;&quot; button2normalimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;0,32,16,48&apos;&quot; button2hotimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;16,32,32,48&apos;&quot; button2pushedimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;32,32,48,48&apos;&quot; thumbnormalimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;0,48,16,64&apos; corner=&apos;0,2,0,2&apos;&quot; thumbhotimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;16,48,32,64&apos; corner=&apos;0,2,0,2&apos;&quot; thumbpushedimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;32,48,48,64&apos; corner=&apos;0,2,0,2&apos;&quot; bknormalimage=&quot;file=&apos;scrollbar_v.png&apos; source=&apos;0,16,16,32&apos;&quot;" />
```

## ����ͼƬ�ļ�������ɫ�ı༭��Edit��
```xml
<Edit name="edtRow" width="80" height="30" bordersize="1" bkcolor="#FFFFFFFF" bordercolor="#FF4EA0D1" textpadding="4,3,40,3" textcolor="#FF000000" align="leftvcenter" />
```

## ռ��ʣ��ռ�
�����һ��ˮƽ���֣�HorizontalLayout���У���Ҫʵ�������֣���һ��������࣬�����������Ҳ࣬ʣ��ռ���ڶ����֡������ͨ��ʡ�Եڶ�����**width**���Եķ������ﵽ��Ч����

���Ƶأ������һ����ֱ���֣�VerticalLayout���У���Ҫʵ�������֣���һ�������ϲ࣬�����������²࣬ʣ��ռ���ڶ����֡������ͨ��ʡ�Եڶ�����**height**���Եķ������ﵽ��Ч����

## �Ϸ���С����ʱ�������ȼ�
��������ڽ��������Ϸţ����Ϸ���Сʱ������ͨ�����¹������ؿؼ���
- ˮƽ��Сʱ����������ˮƽ���֣�HorizontalLayout����**����width**���Ե��Ӵ�ֱ���֣�VerticalLayout���������С����**��width**���Ե��Ӵ�ֱ���֣�VerticalLayout������������ˮƽ���֡�
- ��ֱ��Сʱ���������ش�ֱ���֣�VerticalLayout����**����height**���Ե���ˮƽ���֣�HorizontalLayout���������С����**��height**���Ե���ˮƽ���֣�HorizontalLayout�����������Ӵ�ֱ���֡�

����˵����
```xml
```

����������ù�����ʵ������Ӷ�OnSize�Ĵ���ͨ������ķ�ʽʵ�ֿؼ������²��ֻ����أ�
```c
m_uiPreview->OnSize += MakeDelegate(this, &CMainWnd::OnSizeChanged);
```

## ����duilib�е���ɫ
COLORREF����ɫ�������ǣ���λ��BGR����λ������ͨ��Color.ToArgb()�õ�����ֵ����ɫ�����ǣ���λ��AARRGGBB����λ����

����duilib�й�����ɫ������Color�ĺ�������ʹ����AARRGGBB��ʽ�����ڴ�ͳWindows������˵����Ѿ�ϰ����COLORREF�Ļ�Ҫ�ر�ע�⣡

Ϊ��ֹ���ʹ�ã����µ������½ӿڣ�
```c
// ������һ���������Ľӿڣ����ֻ�����ü򵥵�RGB���԰�װ����ӿڵ�
void SetTextColor(IN BYTE r, IN BYTE g, IN BYTE b);

// ����Ǵ������ط���ȡ��RGB��ʽ��ɫ������ֱ��ʹ�ã��ڲ���ת��
void SetTextColorRGB(COLORREF rgb);

// ���õ���ARGB��Photoshop��ʽ��������RGB��VC�������ø�ʽ����
void SetTextColor(ARGB dwTextColor);

// ���ص���ARGB��ע��������RGB���ֽ���֯�ṹ
ARGB GetTextColor() const;
```

## ������֧��
�ҿ��˹ٷ�duilib�Ĵ����ύ��¼������֧���˶����Եģ����ǹٷ�û��˵����ôʹ�øö�����֧�ֵĹ��ܡ������Լ�ʵ��Ҳ�����ӣ������Լ�����ʵ��һ�¡�

��Ƶ�Ԥ��Ч����
- �û�����ͨ���˵��б������������б�ؼ��������л����ԣ��л���������Ч������˸�������������г���
- �����������ļ�Ҫ�㹻�򵥡�

��ƹ����ԡ�

ʹ�÷�����
- ������̳�CAppBaseMainWnd�������װ�˶�����֧�ֵ�ϸ�ڣ���
- ���ҿؼ�ʱʹ��CAppBaseMainWnd::FindControl���ú�����ѷ��صĿؼ�ָ����ӵ���֧�ֶ����ԵĿؼ��б�mMultiLanguageControls��ȥ��
- �����Ҫ֧�ֶ����ԣ�����Ƥ������xml�ļ���Ϊ�ؼ���ʾָ��һ��name����Щ���������֧�ֵĿؼ����Բ���name��
- ���û��л�������ʱ��CAppBaseMainWnd���Զ�����mMultiLanguageControls�еĿؼ�����ȡ�ؼ���name��Ϊ�ַ���ID����ѯ�ַ�����Ϊ�ؼ����ı���{name}_tip��Ϊ�ַ���ID��ѯ���ַ�����Ϊ�ؼ���tip�ı���
- �����ļ������·�ʽ�����ü��ɣ�
```
# lang_zh_cn.ini���ݣ�
tab_setting=ѡ������
tab_setting_tip=�������

# lang_en_us.ini���ݣ�
tab_setting=Options
tab_setting_tip=Manage Settings
```
����ؼ���name���ԣ�����û�г��������������У�������������ֵ�ǿգ��򲻻��л��ؼ��ı�����ʾ�ı���

���Ե�ֵ������\n����ʾ���У�\t��ʾTab�ַ����ڲ�ͳһ�����ˡ�ʹ���������������ļ���ʽΪmap��ʽ��Ҳ��һ��keyһ��value�������xml��ʽ������Ҳ���ÿ�������ת���ַ���

- �����ര���������Ҫ��һЩ���⴦���������ظ������º�������д�Զ�����룺
```c
//ˢ������
virtual void OnFreshLang();
```