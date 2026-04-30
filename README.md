# ascii-excalidraw

> Convert ASCII art diagrams to hand-drawn Excalidraw JSON files.

<details>
<summary>🇨🇳 中文说明</summary>

> 将 ASCII 字符画转换为手绘风格 Excalidraw JSON 文件。

</details>

---

## Overview

A Claude Code skill that parses ASCII diagrams and converts them into beautiful, hand-drawn style Excalidraw files. It analyzes structure first, then generates JSON module-by-module for accuracy.

<details>
<summary>🇨 概述</summary>

一个 Claude Code 技能，解析 ASCII 图并转换为精美的手绘风格 Excalidraw 文件。先分析结构，再逐模块生成 JSON 确保准确性。

</details>

---

## Quick Start

In Claude Code, trigger the skill:

```
/ascii-excalidraw
```

Then paste your ASCII diagram. The skill will:

1. Analyze the structure (boxes, arrows, containers, layers)
2. Assign semantic colors based on keywords
3. Generate Excalidraw JSON module by module
4. Output a `.excalidraw` file for [excalidraw.com](https://excalidraw.com)

<details>
<summary>🇨🇳 快速开始</summary>

在 Claude Code 中触发技能：

```
/ascii-excalidraw
```

然后粘贴 ASCII 图。技能会自动：

1. 分析结构（方框、箭头、容器、层级）
2. 根据关键词分配语义颜色
3. 逐模块生成 Excalidraw JSON
4. 输出可在 [excalidraw.com](https://excalidraw.com) 打开的 `.excalidraw` 文件

</details>

---

## Examples

### Example 1: System Architecture

**Input:**

```
┌────────────┐      ┌──────────────┐      ┌──────────┐
│   Web App  │─────▶│  API Server  │─────▶│ Database │
────────────┘      └─────────────┘      ──────────
                           │
                     ┌─────▼─────┐
                     │   Cache   │
                     └───────────┘
```

**Output:** Color-coded boxes (blue/violet/green/yellow) with arrow connections in hand-drawn style.

Live preview: [Open in Excalidraw](https://excalidraw.com/#json=AWpdgMs6dtUKoQ6lUS_UIbpbKruRrYteUedV1Wk2ra65sY6zd6OuiKCbSMNL-zX0dwcY-YYgPnxzZ51Gr_34iVw2_rl3Zhl_g2e0rSliePOmFmptRyzHDHmMIjuTVLzentSWHuTmrgOYC8k36x6sMNRcW7RfUWrtKqsLZJGgZMZCKhQPjYsq5F9fdGOUgSamj8fzz7-tRKXwAddllQSDzx81JIqvHukOVqh4JEjBxQfBgh8Fhaw7Z0p34qdmbJ71m1dTPdd0u2Jj9MvOSc0dQ_mo2Qd2Am3wraOx_E9htjsQE513jOXhEszc15TPfYk60OH7KFfM6PDO3kMxks1gsMqlq8H16jT1yipUFGQo1REwLfGw7_Fy7WjfUMccnfDHIqcTzk4iMeGIxTSryew1wvzKli8mtfi6NRSu7XytEFg_Y6Rnfbdy9CsTcy5suihAa9K3Aeqk2U0WwwI-o-ajtWA9FPoQ8qpdsn80aGEcaRFgFM3oDh9sdLx8Tf5rO4m57dD7L0lEhSdOVQCUhn7S2TtSOqX8SJ8odlQKv-LF6hYUM-W1Yllw87NHf3NbimWcz9MnMhoJCzN7vqY16POxxrpVdnqbdzsd9YRHvWAfGHcA9v0aKAK3ZZyqD2p72A_Z2rGRknCI-CheutKYyNR2hsbEcUl8VHHcDWFkqZZjRsqIyxAmDep-rV3M_V7UdifUm_CdL6YXz-MbaoChs1DKHY_zmapDKfLu4-eNk1yDGj95taNiuelaVIR3Ek9uIePZUjCaeQ4BN35DO80f9Oo6PbJV-w9OBLnE9Uh7Ha2kq3Ib0M797wfUUrhoF_KdjIW2Gfgrrd5ZDGGpHLsbtPbTn5hZaW0DNSYP0RIqZGIevvyRsMIBIwii-__Dt89OIevESG9Q4CCpFOIG-r_3Jsn9YRHc9VUPck6phDqvkWieKTa7DTydhm0lR7koLC8pvn2-Wefg7loWMc_Gi-i_-26knB5iBFwaPLFLoAjHYuTneiuMXXy2pd9fBDv5N8rZO-vLVf4_tudDg1nc4EZKdcPHL9zX89Xw10SmErCS0fPDSV03A30Kcbycca_9Po-yx3HaUOBUWbXHzM63ia8XthCHxOT4lu2gxNr-TD14IP2xG_9-TeeDH8BPkzCkArM5WOtUO7xi9tPJUbQ8RrwRfffUZCxOlXD4GrmFJmBMHv9UqY-ksxZO730OJu4AkKMCJ8ZWH12MnnxBR6nWc1Wf0s30MsvW26ZVrw_YULMsn2WkNB83okl6Wxv2RepzmET2virNG3wOHy6UMyVBrIVkxVulCLJ7Ph5IFuC7tMbXAwE-ZR5FuoCs_dXW_49RnOFAOZ6zEm7W41qryfwcZJItZxLCe2qns9ELke2VWhJyobqXTWsaZc0ql2vOs_t4FutZbGPW77enZ_bCu5rUMKLg4WxNFByuA83bXKuLsPKg_iyDmCJMcVvKh7_Y5cE4xoThNAA-o1s5asbkDoHDnE4OatOEQdVGBLfCh7HYHsM16INMmD2jeaCLys21szoZ_XE7kdFYri9yjtMlYrk7DooodOXMAU8C5cb93RGbE0DBDD3aSh37MW6h8-MIJw9aogW2mLnGwuY7XbOZ5kGXeuim-JhmjCTebBmxAN5gVHY1xmM0UxLea9dG4Cd9r98qK9oEiP4dWmgix8iAh9Zs5nJa4aHVNAZB8p_H_ETVu_zHjpLxMCOD9B_ws5qBYh97451YKMQ2vqK2SpWVWsyNWtoBXuFcckH1tK5fxT7hfvr9Q3fOERyZwHfZZpH_FSrIGP9WeOU1al2lGhCiyckjOwuxv9cnEZ3CbYrBQFMe6SeqnZjJaev_dM5LAVZV6hOB7-qmYphsx57gemx2ZsRaiNjjm3tkyULHWawn_2freGAfGNwKOivQ79E3wPQbmOHLClw6YRKTMQyV0S3ne3GIQIUiHUwOXrY5tBvVqzwU8m3Bs55-f9ZREzSRXmfcwZdO7myMwSZr8MMya6-nf9rhyyF6NXwitC-XPpIEA_3_JZINYr3myDc9kvNcXVNDqWIyuajAjhUvgif_71CDWpvMCFfC6iuCQNYn9_vkuxVvFzt7tqHSYikBoNBvVz2LPOSH4oDp7Hq1Qu_3MZwB_6uAyUhQhlVsPkikfMo1hyEJ8pcBCY3bCSdZuwIAY2iz07JqGtooEgQIq4YZlzwMp8SBSs8Zp-tWjRC7-Ppx7suQSnQxeRb7DagoFxav_9gBdFDRuKbbtdddte2zbuCsyAbs5B5ORtO3aR3eKR822kMvg_zeyNJ8-GIDy6U85il65pJo72x0xKz0QQzSjdM03cTmP8gb3jQEZaU7_CDf5wz-VWANM3wfBF9MUzqqIyWQcxTQOtS7y_1inkJMz8AT1wXt5VvdIbRfgTDW_-FDt_9YgZjhXqCUvfu42V0JqbCm6VcEzmFkpZ6PHj6TjkGUlKOaIyOvNHOmpaAsIYspiu4al6McjOoWcM1CaCuzvHL6u-YhwuKJ3XAZjrFls7A_Uthy0Eq4hihuphgE0NrfmZKz-cqVIa9MbJkQemIoY-5ZCb-IOBrIeep9cHOZ39n_o4aSijgshJBHzF45f7NE5L8YtrHz_1OxUCXFHs9bizkOXgyouhzAP-fy8w5NTV8jPn_LDLnNRu5HXEOXezmr8zLi94Tccw_FDkEjuC0Z0tdRPEuzD4SyFSlMhkmiFh_hukKy9Wzr8Mzhi9tpkGntGqXIg5qvD_eNgNQ9nCSNMJwl8-kMtZHbP6TLygForSk2hSRYY5IqwG2ZeR4BQ6e6jC21v46EO7nCYaPDBY9XtsA1vBt-pUB_TxWcivyhfNdfwJfQCj8hGLuPyfL9l5vwK2DIcJPix5r7wOKlomJa5_ssB_iXsC_HK_64j5DtZyBq8c_0bGuJBZJqpBVLcVdgDZW4HlVjmCUT9-REM9oSDMVwq5sGtuBQu53sRNzM6iTsBfpQbW7LDe3VRKXODyjYi3L_Xfv8HP4KHHNRau35XgGH-zl2I6_gkt2rhioILbBq7VEkVVKMSRHEyYSaqraU-OtqqNXN6Oy0uyipTWqU3iAASfHYAJPElaAjJwo6GjkhwO72LzvvqwBigSdzTq_5aAdIctWez8yUyLeFXgYaFZOQwVfXhDzqIF77gypDHxPRLsAauNcihoE6LhkBqJqfLE5LYCDSohyeCtFg0DcuuF89vKTwgHR5MbdLjYPOR9kV7RN3c6ec9fVVsdgO7wZI_hSEoJ3iC8uUYCyB4XecYB-UjYuk7_lAIHLPS1rva5aU9HlEy3xzSi5ec8qB7p-e5Ce9BKJRJXF7DQbe_rSGam0ykupqz8aS4nUXpy8xMiRacvoRio4UfuUv3rt7O8yPl_3lJ9KnRy0YK50r0O1UWaCv7JEYrSM2t6BMmDHCd-miI1XCSNTD9UMV56nd5JSp3EbE2rGXVwlM4-hFeEnbZE18w8QyWsF3h3Xm4isc8KbFwigz8cvrm2a-DhCWuB2Y9KNyQlHTY8bLqkH4_aVbum0othoM3HwDntJWtX8UHlXoYNogDx_umszoTWLTqp8Il9fR0vXnnWGZRN1Ixpa-Y000ma7uL-tOWtzfPDQJWgImUifLk7GF0gAqp6J4hlDGqgZsbSUoToN8p8o7qJRVtvJOIFXgV02HPLKW6UDquMPSHSTj8lohjC7FJD3Q1UHFzw01PTzFByAFvWZR_Xi4jje7azdgnLKRL_4bwSE37tf2C7DRIGLG6mOwr7JGSf1foKYpoITCiPsLkSaK4wyEq9FmXRL6XKzlbSn6b_GMMxCCD9FVshDt6Upna2q7E12j41HhF0uST26Z1bVU8t2Oer3XieV_STP4kOAuWNRBTxi3ACQEaYxR8WHHK0YbkNSPwyBSwZsofYJve76MPhcosnX2QN4tP1008giF4lfr9qCYOrQdd0apqV8iJm6llW8IhSUeVPuos4WTZybCkZSY-nnz4SYZuEy0yNkmxSEWyWhHF9BQ9sYm8aPNgOrA1AFWyZcfTweydI4WgNifkKk1pWxDyE3g2mbXqwk58xZA-t_WuFrroz3C7-7DCTpXkE_MdqcAEAgSRSCBwwWPAtKdM8dYRjHA34mmxUKs8FdgJkzHm7drGTa5e3iSW-b00jkJYDaRC5e5n5Y4BCWLkm80hhsPuVjkGePpbOMX8MGTtKIMmAspxjAWrUIx-nqgUKyGx8WHLzw4h_KtGvzIOszgIZUtWzjlETJ9SKum0PSGxUFr6sNCAzJLkq9UFQ8teHhvX4sETldFz0qXJXy8TEGToI35KVbWwkXR0q59I4_N8961GryT3RkVX0BEeio3XCdtBkI40eRfw6FOdVijKryy3EoaiFi0HyF4jQHeGLQoU-ue-5IHnZGmX2RnEJBQrt3mQJyUjetUZQK5IrmlXv6_Sz2yaCjcoUdMphE-noszcSdb-I_qAPY63GTPjeSOJlnIhqWJPLxlWobi7HAoy6dATo18SPi8b00dNFHG-DIgeIAXLb4fiLTntwzMlgaB-74g9_asRrNut2isEoOmjvt6phDTq4LABEJsxZWNoI6OovkazFhzypP4AQ4BVh1GVbuNw00SzzjrPKvLuEH8O3cGckb1BaLi9UOYRNyYbXfnsvGZemwP98_GiV2JQLP-E8jT_MS8PlrNIr01e8EvIrtXsB_qrm8q5VKOlcvX6FTwNSlZpZ2eY9RQMQNTPZ1020b5uZ-C1Ag0WyAHnlC_fiy9xN_L6UQce8w4V8ciyV6niGThe9XH7TEalaUXziNKIzWMn-habxBIYc2yHQ7AcM_LNd1OeMBHggrUXA1Z7oDVm7cYcSBelmHyjZOvudyflXl45kX8zIIAikyzGBbv7V1n_n53KjgiKvW1CkEi0dkCSUjiDEbygtqpQsWdM9cENeD7sCon3C-8Lmoaf_imQAcWLmqCTbASv9rMY5NZlUWXbhDp_xR8iIxTvnjr9PhsTKbWR2YmjL8zuPRz2HiyUEjC57bulRTaYeke4y1vGSaoMa0QWEeDJrRU4TH81rpWzEWb-I9W9d6gnff9sSxvgqE7TqQU66lt0KoUQ-qt0zVh0R78fV8XZRexWeSnW4hNuQYko4IEP60o-qpUfp1LXOofry7GWGZpNRJYQz5hMRgpPZwrGOBdRYZLuAaEIMBYYjFiK9sE2hWGw0yLZIVm1dQfCAILkRM4O1WuOZosjRI3SRxawUzTCj09TEwhl6YTjLM5SuRyOZ6d-3WKdlRGoESc_0Lmc3virgdNt-QE9bTzSm7zxwhIGVv0vHbe66MRkww1P3oyuoBUWjAY_HKQf6mzK_WgbDss9oPRDmYbUuGKgdThbz-_Pf2aqZ69JvhENEn8QkTVr96OAACQH_6nJ24VyLT6RHXYPnyw6QOYKhfKvhQzziju-E6_PxjdD86TsSYq2rxWMmlj9TlwBA9s_JF907734C94kemdxq-NQJhHnrzTqRAxwIAIfWgT14Ooq4GWEQQ_KvyWd8cjBFVLIXdZF52_7J0xyyVajZGDguamYj3o2_hgpA6HBg_dcf-cdrUBEooPu03Y_Oe3Q_cQxHqjl3xJ6SYRrBGiKIJ95AFsYdA4jCl6ReY_n_vNRxXt8z0zO9k3lQH4hMY5dcmj7UUmMo72LGjAdcx-x8h4qe9lYdb8nLQYMdjrxUwKCIyf2rvI1taPhJIk_wNUKqlVNX8Hex0204MAaHm84C5h4gzqTe__r896QHeBL9DGlGJvOM1U5kNkS9l6R8yB73Cy8eETqIqPtHiOiPUlGU1228r6vrTsSCCdql79100jJneTuAm1mruan2Zby67GZjUk6cAVA5rW9322XVb5LyQazdjoj8n4M-hv9ElgSYzgBzYIlpvuDO9SQenK9nJiMEdIJhrHFQil2GntBoc-TSCjiPErfcyV4ocyVztg8R90OpIr9NrSzHW-lErOB6h1PaICtQnavkgcWQ10_LEMLV5Dw8f69er4PF3OrqKWCO7-8EZK4HNTFgQvGJLLfoDNSkIxXzgmBVblhUuLOFrjxagY0_M4BfTQBzffADCkJroHwbOXxKAFDYcGmgb3r2IlMDkTOqqu9tkmD8MamxXGsj-PWvFV4BTxKkJySdYQTOJAPLackJMyU6RsdQl3eRVMhmS1tvViGQho6CW7Mp9UPsoKgryAco3HvzL_bQvM7_WH-8TIraGLLs_Gem2-kgAgmxO32au2mTfiBLf9Fm9DXB_qaHlAqP-cRkbLVQdZxo0c3PBsR-41v0NYRwLtZ0K1sUGFyGUGERjvRjDdfFotBQTGbnNYThZdXUtL-YGVz_xQE-womQ_uyEfd4DHJAd1taTDOLHAwZrfeUF_09Os5dVtJXMxDHzoKu7UU1L66XV5k9IZyGT5Kb-janHnD7Hd2q5toLMP9DbVoU7_yfp8K_OrzISJ3QonwOxnFb5YFIm-PGQO1GpH7lpWyqklR5a7_HtJRdUgqqJxnSIxy6gwZemnkEGfUIHKXZWVQyp5LOuf2NOn8U5RK-OIO-YVmHDS08EgJ7TOrhyqegz4eaVowwf8SF-J9U6hBoF0qgJjtLvy1xznGQ2MIW0b2_Db_TdSD8krX1afMOvcZkzm1r-9IqPof1lD43xQF0ZdQwmHaE44VunXB7dJjzQgBULE,016a5d80cb3a76d50aa10ea5512fd421ba5b2abb91ad8b5e51e755d56936adae)

<details>
<summary>🇨🇳 示例一：系统架构图</summary>

**输出：** 按组件类型着色的方框（蓝/紫/绿/黄）和箭头连接，手绘风格。详见 `examples/01-architecture.excalidraw`。

</details>

---

### Example 2: PPO Training Loop

**Input:**

```
────────────┐    ┌────────────┐    ┌────────────┐
│  Collect   │───▶│  Compute   │───▶│   Update   │
│  Traject.  │    │ Advantage  │    │  Policy    │
└────────────┘    ────────────┘    └─────┬──────┘
         ▲                                │
         │         ┌────────────         │
         ─────────│  Evaluate  │◀────────
                   │  & Check   │
                   └────────────┘
```

**Output:** Flow diagram with color-coded phases and feedback loop arrows.

Live preview: [Open in Excalidraw](https://excalidraw.com/#json=i6D8GOHpEs06lCMzZJUfazWZKtTXXe2risuTnGZluHzNlTyBwVlhaaNEzm2nZD27oqJuoCXzU3isq0cLhHU7ssGpSRvn9kBo44LQZoNqTfQZRLgHSYEZFOhdEqtE3S_WYbqmf5VTBLh9QbJPWIoOOWHim15RhqqrrCe6MeR9FeK3OhFwryVvcVU64wQDx8KJnYz1Ry8A-fdL_djAejMeFHlr-qOmbAdT45aVvD1m7aI9-Lj5Mi8uXqIt3cMWeqhQKJf8BJAx9JgDJCcnUZ0HAg3EmU06sasM7ghuq34sbJr4N0lj3w0ohQISMkjVI3FudAx3a8X2Ht-KfHw3D3q7GE0Wk7B_6oRQIdbOHSkdEY4IAj1MN3eD997MkDu4IDLyQvxGlN56bkCQEKd1GWnUiU0AaeClHUTTzzplhBHXmGOZY_BA8ts5tsAdRGGs7YvVya7AmCb5bseUQYyfFvqkcPw3jC_JwHIonTOvX7cqalI3ndaGFrlx080-cUJS9WF3uUtO7LLgFh9WSCarZ87MFEN6kxlGNyQNPKAU3V5UKB7dCCueOObHrIPMBAiEaQVPelexsfSpa79hCLkT1Yd9yjvDJPYqzqv5c2Zdrve2dnnkoG5nczNDstFG3Ey4DAIxORDTCtNmnA3LHA2CBVdjuHgoj9zEQ4VvkGiK9QKUZKo9Zh_WS6e8Vpl54W8D7ub9S2MVMSUZbe0DyT2pVspU-PzVX1r80h-YAPitFVN6hqohsyXbLOjBXC3krwhOr_R2-uIskjlDXJZPp0veTqjxL_R-9I_DQ0EdHfONnnwkNZpa7JAQydpDG1KEA3VbLZ9DEpsjY6Ec3WMvK7KQtjZ-r-ovpHt4c4Qsr-4JsX95MW2TDBiv6FmkurjeyudLE-OVpUSsoGev28GN8mF2cXi5NC9iQtd1UjRMrOkNw0kXBgpaH2y0xLhqbqF1u7SAoaFCvuldiW7cmY_dBNSgQrhOarXHCjxUE-mJeZK6vhSjiQpxkFxya5IiFJ_AJIuoX74oOqfplI3yeRB90E03OJgWp8M0aZiggmoCZUfVqrQYUtQU4Oj0GjpmBJhNyfl1WWSxTvUudMNbmm0TByT5kkdziWU3FIVd3RhBbrpt9va4tp6SIPxb3s61VBZLplOV2W0r1VNGKrldLFFnVbr53o1S1JRVFTLJQSUXKWhoIiZ8aCteDVmLobHhxnXU-ViBRvRBL0Tfzp-RDTYh_p2CaHqGjC0MnSiX_KmeNSl4-iaFbfel8gKB4AcdetIJPhTBoxUlTsOCZkupsiA8g-HM05App7LuiEHIr2vaTRWpn07YmcPnUzf0N2HxUPuTXXfzg_wr8hsV-WX2SGfrIR8Tzm4s0G0STVnMV5gK-Lc_bWmOYFYJP7YxwBr6mgGrnBaz2YDuTbU7z60GWdNkkrQlYdprydfVEu1UaZA-h9ukpyLErUd8kOtVuWEJ5AuxJzLAJO3jsOOz47OElNa4OO4Qt5Df1eogm1_ilF26DSTsl1Vpeor5nry4cZLYb5oTx63ijDJduWE8VTTYSw1x2E8ZXRrIj9MpcffRWp5rmedTN9ImHxx7tF8yRGX91BJ4UOl71UItQlS9_RUu6lTKvkU8PB0xmynytqtmBc3V8w-BnY94uCdOFfH3UVaDWMLEB5KXS0rLiPmJXgX_goni-3XmXR26pcU6eIe2NkJnAxbgbEAWWz7RMl9fjXa3t3xV7AflXenRoCnSZlm6D_URWL1GTta1JtECtAgbQfFY9GClBhl3fbNb3mYisKl5oTFUyqUbQqvDdiV6mGpkphzxW7dtadIav8dDNvcuDiY4pkujZLkC4Q_UwnsGGt2FlgoUri-2w89K9o5ghw_NjTcIc1RrWZwLdz36wHvigm89zU3qNOA1D9VJfLZzlYDjE5qfUK2QZBIq430IsAluTq4_5x5P0x7utwbDGCgHonIx9C-zO6EzAOURUKGqUYK1kG3xNu-DGThPBy4EYHtjTIZBaqO-fC3kP6gNtV1MHliziDOxg1oUqItx5xFcJ2qLm-b3Cd3_eRjH8A1s4O9JUkLoW58KFMNMsCLQ-tYOF67EjlS-kUjrHjc_CS4Dk8OwH-Ag8efN65W2e9VBOdSpwEHxWltZo5_JWfUdEAJ-uVu2HSw7744U5lycVbCkCxL4613zK8fvcVlMmMjmELx-Z1yuEQH9JhVRBvPaCF0fQmy2VZj3Hdiii54t-8m-uHBDFFQXu8GKXkN7VJ2E0Xp2o3VRKRlczWWtzuREP5bIP1GTXWEOJfFDkFuPSafRA2kzHPuqwRctEjNBm1WZCG0xwKpwhIueJWjs7aFIEzeYzzudWKLdW3uf26x_7sGbYmWmuXEUquYOhedO8U7cl_0bcLTUq_N_hLOLp1HqtNCGnJW-W-nD7zk5xDJjsXvSMVv0rjhoIWUYTXTgXF4yLSqcpf_KIRWyMcokh8B_GbjgSIECHVsmMJXsd0A6I7rgEPIpTZW2mWOgAZkNJ63y8RMmXn-3RimNo0-XoHtKOIOCgUYR-QS8BhvviV3jBReq3NOtIjofH-R6b5OHP0eD8IeXffoSfm8ZxEP1-OcVm89uuy7R8oFESD2_gzIvR8lFhnqgEmxD2Ty-vcbFJJ5aogLvsuB1YmY5ZGW_sZqd63XuWRD2JQA_0_0N24W0UdLb29Wp-WwOX7sm1hkA0JUMEiLqL6iaJLKwAPouRTTZAqQkjcC7qNX2l1L98b69GKGj46zY4dap_slU2eTR_5AwsfhnvKn00GoO3KZ_H21Orfxnrl5U6Qmk25I--4FCqkGcku3PVQv2zf2dKEgKy5QBO0aUMF0OsyOjwCgllNZtoGlHY7BsJ1Q1p4XM7MGzJYNuP6xAqF1hy9WuIWQC1xDe2iRI9nBQa-kR1OG-wErYM-symAhyjjePlJFDIg3g56XkjB5qgKYLHShIyLUpQsI2yb43eMwH0Ce5EgWvaH955Ncu2ySUyFcy4vPOeHk1Y_esCNI1v90Cnnytj89BSo9rXuRPF88OsMB_zWWIxG32VnGWKGaAplBfVwczEPyTAbcI6pzXShkC2i8Q6566Bqkhiw7NfmkA9UDgPjokKqZj1KjnJhULDLoXKyMuxjSe_kMggrv8B6DalfHbw_4LqJEDI8uhthTWHsZdkX8hnGS4dTDR-ajiMC-vQsWh9G4UDrl9RgMXklKtKD4CICx4-6rzHEuaFWH3lvffVw7aJiH0HmlOhwkC2mPaxRAFj4OWU0F2DPlnm16D6JmS_JkYYHQ-VOR04MLK2hX5azHSSrVCbgwrEQiDcXcXMETJoklm6fNQIvqze9uIUzTIDjyMRdlkCRkAXgKFonwV2PDiQGAn4nMgtbWMLWiGSUVQk5KaLPHd2gi_UIY-J4FSYgQkIjQFMJ2gN9imvo3Vcq4Bh80h3KvdtYv6iLcJYgRwzsCQ_1EwZ3pnA7foBuiLG3353qKuHQDr6OxX0FxczXcsBP0XOYzvtLFc9w5G3wwx7C3iEsG-uPEm2DgXo1fzxVWKVMq6XDAu0-kCAWRnZyaX8UKZi4Uzw9fRe4f6kwsOf0Q3Lc1zIzYOrDK8hMzCYeHfPv9sgR-mvcajgH7gY85QuHPNw-631-andPEj9J8_YUISHeIXjBsS74XEZkOeIdeiZhJa1y0LPIpUevlUxur59jsExtonrRYnHnFkpHE_qt9jWvpegvdqoN5LnI8y6q1wax2_mE8evdmwYwSZ325-9cfQPl1HjeHAJv5xvDfl7BHfKuEtLk5W_NfkGH2tPYKN4dcs2hmNCYCi-HStqn-ku6Pd9EnvVEAHuNBktGpma17AfvvrJlDZYIJM__LCwpCUjuzaXLytXSRCqxE8oLb7jLYwnmhLT6ITkx8k3q_lYKH1T-BdEaNaghtuHXrlyb2Ag9wDHW-Wxeik4c0EvMxQf7k8k5agNpLw50Cr_lscARfz2f-qjqdnkoEmzo8BhVkCONfwLQ14CsKx1R6MIC_Nxzuoi-aU3Jqja6AI7KGkTD-Do2bS_vOx6JHI200dGhSnWMsu6qRxU3A1VPk11JjpkrhbvNKIgmnUOBwcbnosovAbJcn-eiVgsa_b8Q163H8cY5ASJ8HNJW4SW3GiYZWQZ_DvNbX_UapxUlwX0wz-TgecKUFjcx-TF1bXt-T-HSwUNc4j2INvATawJixb6_YLxUBEpOSrdds6dS_9W94GS8_xL9wArxZ9uHAVt92wg4jq4ICC3SlK5smHnd1PG3pbRglOEz1CmClTkDK_ZjAmkoDvsRjk_iLWB8ci7_jBA4yWUgmFMKOWQ9RsHdMoLIiDhkvnRz5f2ncRXwMb60UdmbixTTstTbpq5Ce0gBCz1QKVgduMSaRfFZ7KXtb8Ks3ZYPYZYjmKcSXooskGdmS1ArRYia1r_KsQd7Jj20sZy_4XPWp7PQcPki1-Fe2cAtdV4UPST90a3aZNNarU8OlV3Cuf421DRmYaox6PuH-xW1aDDTtIglUcfhqs3kSNNIiteZYepokcprE9YMuVjJXMiqVDRYXp7VADxthyYzu6kRvOSd00xtF9K7J-VegY9MVYYNRoXJzO9AL9hqTb0eP78U-23Dnx-SXsFO36NyFkanP32_TBghhPV-hU3-UjdNt81ZLplNQx77jtQ9Ac110XtAunUK9aIW0Zaqz-SAo1ZuRtuyAe-FHORNtUFIwJg2BXi3g-kNd3fRJ01DJ1Wg5mjsd0IFDgHxC3rfAChoW4jXCc2JEeFz9quRGi25N9Bg6npWaqK6MzFhd5BERS-yA5lqk-xymK3LACJEXl6ctZyZyr6cdk0RKAdhosUBVPXcKmNV5zXiorW3snwoLN0F-9TAnPJV9thsb6t2QtBYemwXqZrlTYJoGN-PYWWJjOfZ_ZV5zkliss3svwheN0UGLylH0wy02A9LwD_ROzjfYr_Sw9Jdu3I-pNnpG3vwMpWMjblN7NaZjQA37zAVhh07U6CIR0fVE0Vb1s-a-UfW1TVgAq2ndY4aBwnNEzkZUHXWzMft9HKBN197B7c35xFUPgKv_6_7FGMsRBYdu7mXAuB5GTbPKnYfT16AVjZAdpxRaUsS4fb-U5q_8bzPWgRvBAZlFGrcG6BIIRb_ozphhf6SKIpT6JVPLFur2g1clKUeuMvHNiFDdIAvH2jz4X-2Nc7O24SIU-4PVlhTcDKitfvyRvbM0ed6G9Qv_adMN0F4ugCtiHgtLpJENYfiKZ9lafzksHFsV7Ov_dVINATVArb1-3P-aF-oMAYrQma_FueSCLK6pvYyR8-exazuksQrSmdj2VykuZwKyU4O4HpO4ERvw_kQ0KiLe_RDHaRPCLyGi8v8oS86MveHL7Lra-ZcyfNrMjeBa59CAqSoUwZNHmIy-tz_fUVxDWnXLugqkRCthGFacrH985QBG_Z1LEOj0IIUgnGVI1t7BgLRjqSY4BEMqIPwY6BCQUxjsM65m9PdoykiTGfUQDOFQmBLj7aJZH666h5dKM0KHK49VYBuqcw4P8olNOvi2Ly6CHVEWeQ4UAAAVspAwOu3BM2zv5YPRawS4ZyET5KHr3cW5pQ3LdH3-DkTGGbvhyiHphNPKogpGclHKSkvly6htfac9gs0chIR7yI_NdREq_BAV-j--riroEgIDXVUJDc3MNlKIshw_VvWHHUfeSBiJ9_b7kcG5vHQFPKCwugcq8HOMT27b5T5BozWMvJx3nOWyTcoriyI0A3iskz_vKosZcjmF5Tstl0dSOJLndV3NHYgt0Kt_zHDAFbV8ym9cN8VCao2WuyfYkNM_i4Dxyix8Dp5fjleuzLGxn9c6wg69rm3iOQNzdFf6KIbjgCMPFlpkJKeY4HheeqnT5r_wSlQ81Zfe0iQOwwRodJ7fFSaHww8gJ4w__kUE6pWJehl7-jrksNDeTfe7iDW-bJBNs250CqNK3MM0lcfJ7M4aUIIhtQx4t2mVZLXJzXN9vE435ZwWDYb1ofRUWYqn4dGXvbFjSSu-6tSIBz6vXkwD5U_j1ohnME-IVUPXPWZYgsNJglqq4stJH2AtFVAlaYLZYXBF2Y62B1hSyhutNhLIIS2Ax6bHCBg3WXbZ_fvcHDOeXpOjwWxllFVk_M7hVFK0zP9oWhlT1eMXx_Stj1crfgN2WrVDNCz3Il72oyZrgkPdaEOvYelijy3laWhU6WV5Jj_16d-ptrwOoeU3bUzAoK_qTHWzxAGR0piZNUJvLq9IzHwXh0NSIRQCv-P8NAWuY_B5qz8sVcxvsSee17I2_15YlPukOePydzZeGMdUP1vBYtR5jn2AFBgOQy1hDo3BU60VkmOh2yTal5Y5pJFLofsLlGckqSedazzMKCt88ufKHrmhTaxD6YaD8qWfhEbzSC5U8CV6dFvNIA6BCMtxasIJQEEb1bxgwBpDZ9if--H6o5824DBu3w21QUBLf2GaSx-tvM9P6Xz0cJ28yTSw_6GvUhukvxRl0TuXlOeLM22qqd91e3mEXm82WIKxLMM3wxd-hVgWVHiUQ_4a8oQuTHHD4ZUNrnAy1rfSxJppCtdyZszXEnix6J0xuqUidd54vWvZGWtvwVTP8kwp8787q_pMk_FIb2GXvX_e3xilb4KRJhiUXTa6Yc8aW992Ug8n02kjzagGqyp06EvTSxR4rcc9qIZO2gG23bdm-1Wi6F0acOYVL00LBOovJzO2e5wKrffr3U-YfCZwz5M7ak5E227NI05uH7L_aQr7SeYyHYKjkfFb8zc0OXTgN8bX1Rb7GSedNwlmkZ6Y6FZs8wTBIeIbgFb33-fPRqBMQ4XF4vh5QDA3kBhsQChN5P-cal_8E5wOGR8mMtXedBlBl9sFnE5Ytcf104sTtR5xYcja7M1Iu5fylKA5trFzD6pruIrCpNvvW06Slk_UGmmZzoFFNTlg96-hUjd9ZFjNOUSOvptCB99xgflKyKiQOk4XZ4z8g8G6ZjEFYtjKFw_Wr020azOe9mkH77soZDNH8Jzt7PdP-TKJ_tD9eo41FMChIxCK35xFN_fcZsfs4lWTUwN7OWWrrCnrG36g2nG22v9mAYRE9eZ4e4_ziZNZTOp6d49c7KMdJRTpEGCiahbIzwAcClZX8Svjceia07ZHjFUNgB-fMWQ33y03RS0-j1Q6Ef6ypUNt-brKrnrRY8gnO_7kBEcJD9buBVMgb0XE2aipRMiYcOaiM68ySzFl9sBCvGOuQiwVtImw3Ns6wjK-evfysNcDxEsMsZxZl2VOC-fqmjbVWHWvofPCSvS8rjkUPFQVMie4_g718jki6VYsYjg,8ba0fc18e1e912cd3a94233364951f6b35992ad4d75dedab8acb939c6665b87c)

<details>
<summary>🇨🇳 示例二：PPO 训练循环</summary>

**输出：** 带颜色区分的阶段和反馈循环箭头的流程图。详见 `examples/02-ppo-loop.excalidraw`。

</details>

---

## Color Palette

| Component | Fill | Stroke |
|---|---|---|
| Frontend | `#a5d8ff` | `#1971c2` |
| Backend | `#d0bfff` | `#7048e8` |
| Database | `#b2f2bb` | `#2f9e44` |
| External | `#ffc9c9` | `#e03131` |
| Queue | `#fff3bf` | `#f08c00` |
| AI/ML | `#eebefa` | `#9c36b5` |
| Auth | `#c3fae8` | `#087f5b` |
| Monitor | `#fcc2d7` | `#e64980` |

<details>
<summary>🇨🇳 颜色方案</summary>

| 组件 | 填充色 | 描边色 |
|---|---|---|
| 前端 | `#a5d8ff` | `#1971c2` |
| 后端 | `#d0bfff` | `#7048e8` |
| 数据库 | `#b2f2bb` | `#2f9e44` |
| 外部服务 | `#ffc9c9` | `#e03131` |
| 消息队列 | `#fff3bf` | `#f08c00` |
| AI/ML | `#eebefa` | `#9c36b5` |
| 认证 | `#c3fae8` | `#087f5b` |
| 监控 | `#fcc2d7` | `#e64980` |

</details>

---

## Features

- **Structure-first analysis** — Parses boxes, arrows, containers before generating JSON
- **Module-by-module generation** — Each component generated separately for accuracy
- **Semantic color assignment** — Auto-colors by keyword (web→blue, db→green, etc.)
- **Hand-drawn sketch style** — Excalifont, hachure fills, variable roughness
- **Layout planning** — Text width estimation and proportion checking before generation

<details>
<summary>🇨🇳 功能特性</summary>

- **结构优先分析** — 在生成 JSON 前解析方框、箭头、容器
- **逐模块生成** — 分别生成每个组件，避免出错
- **语义颜色分配** — 根据关键词自动着色（web→蓝，db→绿等）
- **手绘草图风格** — Excalifont 字体、hachure 填充、可变粗糙度
- **布局规划** — 生成前估算文字宽度和比例检查

</details>

---

## File Structure

```
├── SKILL.md                     # Skill definition
├── README.md                    # This file (bilingual)
├── examples/
│   ├── 01-architecture.ascii    # Example: system architecture
│   ├── 01-architecture.excalidraw
│   ├── 02-ppo-loop.ascii        # Example: PPO training loop
│   └── 02-ppo-loop.excalidraw
└── scripts/
    └── merge_modules.py         # Module assembly helper
```

---

## Links

- [ClawHub](https://clawhub.ai) — Install with `clawhub install publish-ascii-excalidraw`
- [Hermes PR](https://github.com/NousResearch/hermes-agent/pull/17720)
- [anthropics/skills PR](https://github.com/anthropics/skills/pull/1068)

---

## License

MIT
