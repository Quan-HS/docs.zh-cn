---
title: x:Key 指令
ms.date: 03/30/2017
f1_keywords:
- xKey
- Key
- x:Key
helpviewer_keywords:
- x:Key attribute [XAML Services]
- Key attribute in XAML [XAML Services]
- XAML [XAML Services], x:Key attribute
ms.assetid: 1985cd45-f197-42d5-b75e-886add64b248
ms.openlocfilehash: c05f98932ceceeb1530b34a09b1923f2af1378b5
ms.sourcegitcommit: c2d9718996402993cf31541f11e95531bc68bad0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/27/2020
ms.locfileid: "81432754"
---
# <a name="xkey-directive"></a><span data-ttu-id="7e6e3-102">x:Key 指令</span><span class="sxs-lookup"><span data-stu-id="7e6e3-102">x:Key Directive</span></span>
<span data-ttu-id="7e6e3-103">唯一标识在 XAML 定义的字典中创建和引用的元素。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-103">Uniquely identifies elements that are created and referenced in a XAML-defined dictionary.</span></span> <span data-ttu-id="7e6e3-104">向`x:Key`XAML 对象元素添加值是标识资源字典中资源的最常见方法，例如在 WPF<xref:System.Windows.ResourceDictionary>中。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-104">Adding an `x:Key` value to a XAML object element is the most common way to identify a resource in a resource dictionary, for example in a WPF <xref:System.Windows.ResourceDictionary>.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="7e6e3-105">XAML 属性用法</span><span class="sxs-lookup"><span data-stu-id="7e6e3-105">XAML Attribute Usage</span></span>  
  
```xaml  
<object x:Key="stringKeyValue".../>  
-or-  
<object x:Key="{markupExtensionUsage}".../>  
```  
  
## <a name="xaml-attribute-usage-wpf-specific"></a><span data-ttu-id="7e6e3-106">XAML 属性使用情况（特定于 WPF）</span><span class="sxs-lookup"><span data-stu-id="7e6e3-106">XAML Attribute Usage (WPF-specific)</span></span>  
  
```xaml  
<object.Resources>  
  <object x:Key="stringKeyValue".../>  
</object.Resources>  
-or-  
<object.Resources>  
  <object x:Key="{markupExtensionUsage}".../>  
</object.Resources>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="7e6e3-107">XAML 值</span><span class="sxs-lookup"><span data-stu-id="7e6e3-107">XAML Values</span></span>  
  
|||  
|-|-|  
|`stringKeyValue`|<span data-ttu-id="7e6e3-108">用作键的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-108">A text string to use as a key.</span></span> <span data-ttu-id="7e6e3-109">文本字符串必须符合[XamlName 语法](xamlname-grammar.md)。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-109">The text string must conform to the [XamlName Grammar](xamlname-grammar.md).</span></span>|  
|`markupExtensionUsage`|<span data-ttu-id="7e6e3-110">在标记扩展分隔符{}中，提供用作键的对象的标记扩展用法。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-110">Within the markup extension delimiters {}, a markup extension usage that provides an object to use as a key.</span></span> <span data-ttu-id="7e6e3-111">请参阅“备注”。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-111">See Remarks.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7e6e3-112">备注</span><span class="sxs-lookup"><span data-stu-id="7e6e3-112">Remarks</span></span>  
 <span data-ttu-id="7e6e3-113">`x:Key`支持 XAML 资源字典概念。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-113">`x:Key` supports the XAML resource dictionary concept.</span></span> <span data-ttu-id="7e6e3-114">XAML 作为一种语言不会定义资源字典实现，而资源字典实现留给特定的 UI 框架。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-114">XAML as a language doesn't define a resource dictionary implementation, that is left to specific UI frameworks.</span></span> <span data-ttu-id="7e6e3-115">要了解有关如何在 WPF 中实现 XAML 资源字典的更多信息，请参阅[XAML 资源](../fundamentals/xaml-resources-define.md)。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-115">To learn more about how XAML resource dictionaries are implemented in WPF, see [XAML Resources](../fundamentals/xaml-resources-define.md).</span></span>  
  
 <span data-ttu-id="7e6e3-116">在 XAML 2006 和`x:Key`WPF 中，必须作为属性提供。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-116">In XAML 2006 and WPF, `x:Key` must be provided as an attribute.</span></span> <span data-ttu-id="7e6e3-117">您仍可以使用非字符串键，但这需要标记扩展用法才能在属性窗体中提供非字符串值。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-117">You can still use nonstring keys, but this requires a markup extension usage in order to provide the nonstring value in attribute form.</span></span> <span data-ttu-id="7e6e3-118">如果使用 XAML 2009，`x:Key`则可以指定为元素，以显式支持由字符串以外的对象类型键控的字典，而无需标记扩展中间。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-118">If you are using XAML 2009, `x:Key` can be specified as an element, to explicitly support dictionaries keyed by object types other than strings without requiring a markup extension intermediate.</span></span> <span data-ttu-id="7e6e3-119">请参阅本主题中的"XAML 2009"部分。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-119">See the "XAML 2009" section in this topic.</span></span> <span data-ttu-id="7e6e3-120">备注部分的其余部分特别适用于 XAML 2006 实现。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-120">The remainder of the Remarks section applies specifically to the XAML 2006 implementation.</span></span>  
  
 <span data-ttu-id="7e6e3-121">的属性`x:Key`值可以是[XamlName 语法](xamlname-grammar.md)中定义的任何字符串，也可以是通过标记扩展计算的对象。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-121">The attribute value of `x:Key` can be any string defined in the [XamlName Grammar](xamlname-grammar.md) or can be an object evaluated through a markup extension.</span></span> <span data-ttu-id="7e6e3-122">有关 WPF 的示例，请参阅"WPF 使用说明"。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-122">See "WPF Usage Notes" for an example from WPF.</span></span>  
  
 <span data-ttu-id="7e6e3-123">作为<xref:System.Collections.IDictionary>实现的父元素的子元素通常必须包含指定`x:Key`该字典中唯一键值的属性。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-123">Child elements of a parent element that is an <xref:System.Collections.IDictionary> implementation must typically include an `x:Key` attribute that specifies a unique key value within that dictionary.</span></span> <span data-ttu-id="7e6e3-124">框架可能实现别名键属性，`x:Key`以替换特定类型;定义此类属性的类型应归因于<xref:System.Windows.Markup.DictionaryKeyPropertyAttribute>。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-124">Frameworks might implement aliased key properties to substitute for `x:Key` on particular types; types that define such properties should be attributed with <xref:System.Windows.Markup.DictionaryKeyPropertyAttribute>.</span></span>  
  
 <span data-ttu-id="7e6e3-125">指定`x:Key`等效的代码是用于基础<xref:System.Collections.IDictionary>的键。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-125">The code equivalent of specifying `x:Key` is the key that is used for the underlying <xref:System.Collections.IDictionary>.</span></span> <span data-ttu-id="7e6e3-126">例如，在`x:Key`WPF 中资源标记中应用的 与 将资源添加到代码中的 WPF`key`<xref:System.Windows.ResourceDictionary.Add%2A?displayProperty=nameWithType><xref:System.Windows.ResourceDictionary>时的参数值等效。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-126">For example, an `x:Key` that is applied in markup for a resource in WPF is equivalent to the value of the `key` parameter of <xref:System.Windows.ResourceDictionary.Add%2A?displayProperty=nameWithType> when you add the resource to a WPF <xref:System.Windows.ResourceDictionary> in code.</span></span>  
  
## <a name="wpf-usage-notes"></a><span data-ttu-id="7e6e3-127">WPF 用法说明</span><span class="sxs-lookup"><span data-stu-id="7e6e3-127">WPF Usage Notes</span></span>  
 <span data-ttu-id="7e6e3-128">作为<xref:System.Collections.IDictionary>实现（如 WPF）<xref:System.Windows.ResourceDictionary>的父对象的子对象通常必须包含属性`x:Key`，并且键值必须是唯一的字典。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-128">Child objects of a parent object that is an <xref:System.Collections.IDictionary> implementation, such as the WPF <xref:System.Windows.ResourceDictionary>, must typically include an `x:Key` attribute, and the key value must be unique within that dictionary.</span></span> <span data-ttu-id="7e6e3-129">有两个值得注意的例外：</span><span class="sxs-lookup"><span data-stu-id="7e6e3-129">There are two notable exceptions:</span></span>  
  
- <span data-ttu-id="7e6e3-130">某些 WPF 类型声明字典用法的隐式键。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-130">Some WPF types declare an implicit key for dictionary usage.</span></span> <span data-ttu-id="7e6e3-131">例如，带<xref:System.Windows.Style><xref:System.Windows.Style.TargetType%2A>的 或<xref:System.Windows.DataTemplate>的<xref:System.Windows.DataTemplate.DataType%2A>和 ， 可以<xref:System.Windows.ResourceDictionary>位于 中，并使用隐式键。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-131">For example, a <xref:System.Windows.Style> with a <xref:System.Windows.Style.TargetType%2A>, or a <xref:System.Windows.DataTemplate> with a <xref:System.Windows.DataTemplate.DataType%2A>, can be  in a <xref:System.Windows.ResourceDictionary> and use the implicit key.</span></span>  
  
- <span data-ttu-id="7e6e3-132">WPF 支持合并的资源字典概念。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-132">WPF supports a merged resource dictionary concept.</span></span> <span data-ttu-id="7e6e3-133">密钥可以在合并字典之间共享，并且可以使用<xref:System.Windows.FrameworkContentElement.FindResource%2A>访问共享密钥行为。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-133">Keys can be shared between the merged dictionaries, and the shared key behavior can be accessed using <xref:System.Windows.FrameworkContentElement.FindResource%2A>.</span></span> <span data-ttu-id="7e6e3-134">有关详细信息，请参阅[合并资源字典](../../framework/wpf/advanced/merged-resource-dictionaries.md)。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-134">For more information, see [Merged Resource Dictionaries](../../framework/wpf/advanced/merged-resource-dictionaries.md).</span></span>  
  
 <span data-ttu-id="7e6e3-135">在整体 WPF XAML 实现和应用模型中，XAML 标记编译器不检查密钥唯一性。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-135">In the overall WPF XAML implementation and application model, key uniqueness is not checked by the XAML markup compiler.</span></span> <span data-ttu-id="7e6e3-136">相反，缺少或非唯`x:Key`一值会导致加载时间 XAML 解析器错误。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-136">Instead, missing or nonunique `x:Key` values cause load-time XAML parser errors.</span></span> <span data-ttu-id="7e6e3-137">但是，Visual Studio 处理 WPF 字典时通常可以在设计阶段注意到此类错误。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-137">However, Visual Studio handling of dictionaries for WPF can often note such errors in the design phase.</span></span>  
  
 <span data-ttu-id="7e6e3-138">请注意，在所示的语法中，<xref:System.Windows.ResourceDictionary>对象隐化于 WPF XAML 处理器如何生成集合以填充<xref:System.Windows.FrameworkElement.Resources%2A>集合。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-138">Note that in the syntax shown, the <xref:System.Windows.ResourceDictionary> object is implicit in how the WPF XAML processor produces a collection to populate a <xref:System.Windows.FrameworkElement.Resources%2A> collection.</span></span> <span data-ttu-id="7e6e3-139">在<xref:System.Windows.ResourceDictionary>标记中，通常不作为元素显式提供 a，尽管在某些情况下，如果需要，它可以是集合对象元素（它将是<xref:System.Windows.FrameworkElement.Resources%2A>属性元素和填充字典中的项之间的集合对象元素）。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-139">A <xref:System.Windows.ResourceDictionary> is not typically provided explicitly as an element in markup, although it can be in some cases if wanted for clarity (it would be a collection object element between the <xref:System.Windows.FrameworkElement.Resources%2A> property element and the items within that populate the dictionary).</span></span> <span data-ttu-id="7e6e3-140">有关集合对象在标记中几乎总是隐式元素的原因的信息，请参阅[XAML 语法详细信息](../../framework/wpf/advanced/xaml-syntax-in-detail.md)。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-140">For information about why a collection object is almost always an implicit element in markup, see [XAML Syntax In Detail](../../framework/wpf/advanced/xaml-syntax-in-detail.md).</span></span>  
  
 <span data-ttu-id="7e6e3-141">在 WPF XAML 实现中，资源字典密钥的处理由<xref:System.Windows.ResourceKey>抽象类定义。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-141">In the WPF XAML implementation, the handling for resource dictionary keys is defined by the <xref:System.Windows.ResourceKey> abstract class.</span></span> <span data-ttu-id="7e6e3-142">但是，WPF XAML 处理器会根据密钥的用法为密钥生成不同的基础扩展类型。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-142">However the WPF XAML processor produces different underlying extension types for keys based on their usages.</span></span> <span data-ttu-id="7e6e3-143">例如，或<xref:System.Windows.DataTemplate>任何派生类的键单独处理，并生成不同的<xref:System.Windows.DataTemplateKey>对象。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-143">For example, the key for a <xref:System.Windows.DataTemplate> or any derived class is handled separately, and produces a distinct <xref:System.Windows.DataTemplateKey> object.</span></span>  
  
 <span data-ttu-id="7e6e3-144">键和名称在基本的 XAML`x:Key`定义`x:Name`中使用不同的指令和语言元素 （ 对 ） 。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-144">Keys and names use different directives and language elements (`x:Key` versus `x:Name`) in the basic XAML definition.</span></span> <span data-ttu-id="7e6e3-145">WPF 的定义和这些概念的应用也在不同的情况下使用密钥和名称。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-145">Keys and names are also used in different situations by the WPF definition and application of these concepts.</span></span> <span data-ttu-id="7e6e3-146">有关详细信息，请参阅[WPF XAML 名称范围](../../framework/wpf/advanced/wpf-xaml-namescopes.md)。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-146">For details, see [WPF XAML Namescopes](../../framework/wpf/advanced/wpf-xaml-namescopes.md).</span></span>  
  
 <span data-ttu-id="7e6e3-147">如前所述，键的值可以通过标记扩展提供，并且可以不提供字符串值。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-147">As stated previously, the value of a key can be supplied through a markup extension and can be other than a string value.</span></span> <span data-ttu-id="7e6e3-148">WPF 方案的示例是 ， 的值`x:Key`可能是[组件资源密钥](../../framework/wpf/advanced/componentresourcekey-markup-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-148">An example WPF scenario is that the value of `x:Key` may be a [ComponentResourceKey](../../framework/wpf/advanced/componentresourcekey-markup-extension.md).</span></span> <span data-ttu-id="7e6e3-149">某些控件公开自定义样式资源的该类型的样式键，该样式资源在不完全替换样式的情况下会影响该控件的部分外观和行为。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-149">Certain controls expose a style key of that type for a custom style resource that influences part of the appearance and behavior of that control without totally replacing the style.</span></span> <span data-ttu-id="7e6e3-150">这种键的一个例子是<xref:System.Windows.Controls.ToolBar.ButtonStyleKey%2A>。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-150">An example of such a key is <xref:System.Windows.Controls.ToolBar.ButtonStyleKey%2A>.</span></span>  
  
 <span data-ttu-id="7e6e3-151">WPF 合并字典功能引入了关键唯一性和密钥查找行为的其他注意事项。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-151">The WPF merged dictionary feature introduces additional considerations for key uniqueness and key lookup behavior.</span></span> <span data-ttu-id="7e6e3-152">有关详细信息，请参阅[合并资源字典](../../framework/wpf/advanced/merged-resource-dictionaries.md)。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-152">For more information, see [Merged Resource Dictionaries](../../framework/wpf/advanced/merged-resource-dictionaries.md).</span></span>  
  
## <a name="xaml-2009"></a><span data-ttu-id="7e6e3-153">XAML 2009</span><span class="sxs-lookup"><span data-stu-id="7e6e3-153">XAML 2009</span></span>  
 <span data-ttu-id="7e6e3-154">XAML 2009 放宽`x:Key`了始终以属性形式提供的限制。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-154">XAML 2009 relaxes the restriction that `x:Key` always be provided in attribute form.</span></span>  
  
 <span data-ttu-id="7e6e3-155">在 WPF 中，可以使用 XAML 2009 功能，但仅适用于未标记编译的 XAML。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-155">In WPF, you can use XAML 2009 features, but only for XAML that is not markup-compiled.</span></span> <span data-ttu-id="7e6e3-156">WPF 的已编译标记的 XAML 以及 XAML 的 BAML 形式当前不支持 XAML 2009 关键字和功能。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-156">Markup-compiled XAML for WPF and the BAML form of XAML do not currently support the XAML 2009 keywords and features.</span></span>  
  
 <span data-ttu-id="7e6e3-157">在 XAML 2009 下`x:Key`，您可以通过以下用法指定元素：</span><span class="sxs-lookup"><span data-stu-id="7e6e3-157">Under XAML 2009, you can specify `x:Key` elements through the following usage:</span></span>  
  
### <a name="xaml-element-usage-xaml-2009-only"></a><span data-ttu-id="7e6e3-158">XAML 元素使用（仅限 XAML 2009）</span><span class="sxs-lookup"><span data-stu-id="7e6e3-158">XAML Element Usage (XAML 2009 only)</span></span>  
  
```xaml  
<object>  
  <x:Key>  
keyObject  
  </x:Key>  
...  
</object>  
```  
  
### <a name="xaml-values"></a><span data-ttu-id="7e6e3-159">XAML 值</span><span class="sxs-lookup"><span data-stu-id="7e6e3-159">XAML Values</span></span>  
  
|||  
|-|-|  
|`keyObject`|<span data-ttu-id="7e6e3-160">对象的对象元素，该对象用作专用字典中给定`object`项的键。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-160">Object element for the object that is used as the key for a given `object` in a specialized dictionary.</span></span>|  
  
- <span data-ttu-id="7e6e3-161">此种使用的容器/父级不在此处显示。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-161">The container/parent for this kind of use is not shown here.</span></span> <span data-ttu-id="7e6e3-162">`object`应作为表示专用字典实现的对象元素的子元素。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-162">`object` is expected to be a child of an object element that represents a specialized dictionary implementation.</span></span> <span data-ttu-id="7e6e3-163">`keyObject`应作为该特定专用字典实现的关键的对象实例（或值类型的值）。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-163">`keyObject` is expected to be an object instance (or a value of a value type) that is appropriate as the key for that particular specialized dictionary implementation.</span></span>  
  
- <span data-ttu-id="7e6e3-164">WPF 不实现需要此用法的字典。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-164">WPF does not implement dictionaries that require this usage.</span></span> <span data-ttu-id="7e6e3-165">对象键是 XAML 语言的一个常规功能，对于某些自定义字典方案可能很有用，在其中需要在 XAML 中创建字典。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-165">Object keys is more a general feature of the XAML language, possibly useful for certain custom dictionary scenarios where creating the dictionary in XAML is desirable.</span></span> <span data-ttu-id="7e6e3-166">对于 WPF 功能（如使用非字符串键进行资源化的隐式样式），存在其他用于建立或指定键的技术，因此无需使用对象键。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-166">For WPF features such as implicit styles that use non-string keys for resources, other techniques for establishing or specifying the keys exist, so using an object key is not necessary.</span></span>  
  
- <span data-ttu-id="7e6e3-167">`keyObject`也可以是对象元素形式的标记扩展用法，而不是直接的对象实例。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-167">`keyObject` could also be a markup extension usage in object element form, rather than a direct object instance.</span></span>  
  
## <a name="silverlight-usage-notes"></a><span data-ttu-id="7e6e3-168">银光使用说明</span><span class="sxs-lookup"><span data-stu-id="7e6e3-168">Silverlight Usage Notes</span></span>  
 <span data-ttu-id="7e6e3-169">`x:Key`银光单独记录。</span><span class="sxs-lookup"><span data-stu-id="7e6e3-169">`x:Key` for Silverlight is documented separately.</span></span> <span data-ttu-id="7e6e3-170">有关详细信息，请参阅[XAML 命名空间 （x：）语言功能（银光）](https://docs.microsoft.com/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc188995(v=vs.95)).</span><span class="sxs-lookup"><span data-stu-id="7e6e3-170">For more information, see [XAML Namespace (x:) Language Features (Silverlight)](https://docs.microsoft.com/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc188995(v=vs.95)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e6e3-171">请参阅</span><span class="sxs-lookup"><span data-stu-id="7e6e3-171">See also</span></span>

- [<span data-ttu-id="7e6e3-172">XAML 资源</span><span class="sxs-lookup"><span data-stu-id="7e6e3-172">XAML Resources</span></span>](../fundamentals/xaml-resources-define.md)
- [<span data-ttu-id="7e6e3-173">资源和代码</span><span class="sxs-lookup"><span data-stu-id="7e6e3-173">Resources and Code</span></span>](../../framework/wpf/advanced/resources-and-code.md)
- [<span data-ttu-id="7e6e3-174">StaticResource 标记扩展</span><span class="sxs-lookup"><span data-stu-id="7e6e3-174">StaticResource Markup Extension</span></span>](../../framework/wpf/advanced/staticresource-markup-extension.md)