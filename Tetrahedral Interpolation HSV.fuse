--[[--
---------------------------------------------------------------------- 
MIT License

Copyright (c) 2020 calvinsilly

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
----------------------------------------------------------------------
--]]--

FuRegisterClass("TetrahedralInterpolationHSV", CT_Tool, {
    REGS_Name = "Tetrahedral Interpolation HSV",
    REGS_Category = "Color",
    REGS_OpIconStrinS = "TIH",
    REGS_OpDescription = "",
    REGS_Company = "Ember Light",
    REG_Fuse_NoEdit = false,
    REG_Fuse_NoReload = false,
    REG_SupportsDoD = false,
})

function Create()

    Info = self:AddInput("Red = Hue\nGreen = Saturation\nBlue = Value", "Info", {
        LINKID_DataType = "Text",
        INPID_InputControl = "LabelControl",
        INP_External = false,
        INP_Passive = true,
        LBLC_MultiLine = true,
      })

    InfoText = self:AddInput(" ", "BlackPoint", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 3,
        IC_ControlGroup = 9,
    })

    --BLACK
    self:BeginControlNest("Black Point", "BLACK", true, {})   
    InBl = self:AddInput(" ", "BlackPoint", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 3,
        IC_ControlGroup = 9,
    })
    self:EndControlNest()

    --WHITE
    self:BeginControlNest("White Point", "WHITE", true, {})   
    InW = self:AddInput(" ", "WhitePoint", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 3,
        IC_ControlGroup = 8,
    })
    self:EndControlNest()

    --RED
    self:BeginControlNest("Red", "RED", true, {})   
    InRH = self:AddInput(" ", "RH", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 2,
    })

    InRS = self:AddInput("RS", "RS", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 2,
    })

    InRV = self:AddInput("RV", "RV", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 2,
    })
    self:EndControlNest()

    --Green
    self:BeginControlNest("Green", "GREEN", true, {})   
    InGH = self:AddInput(" ", "GH", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 3,
    })

    InGS = self:AddInput("GS", "GS", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 3,
    })

    InGV = self:AddInput("GV", "GV", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 3,
    })
    self:EndControlNest()

    --Blue
    self:BeginControlNest("Blue", "BLUE", true, {}) 
    InBH = self:AddInput(" ", "BH", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 4,
    })

    InBS = self:AddInput("BS", "BS", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 4,
    })

    InBV = self:AddInput("BV", "BV", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 4,
    })
    self:EndControlNest()

    --Cyan
    self:BeginControlNest("Cyan", "CYAN", true, {}) 
    InCH = self:AddInput(" ", "CH", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 5,
    })

    InCS = self:AddInput("CS", "CS", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 5,
    })

    InCV = self:AddInput("CV", "CV", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 5,
    })
    self:EndControlNest()

    --Magenta
    self:BeginControlNest("Magenta", "MAGENTA", true, {})   
    InMH = self:AddInput(" ", "MH", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 6,
    })

    InMS = self:AddInput("MS", "MS", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 6,
    })

    InMV = self:AddInput("MV", "MV", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 6,
    })
    self:EndControlNest()

    --Yellow
    self:BeginControlNest("Yellow", "YELLOW", true, {}) 
    InYH = self:AddInput(" ", "YH", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 7,
    })

    InYS = self:AddInput("YS", "YS", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 7,
    })

    InYV = self:AddInput("YV", "YV", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 7,
    })
    self:EndControlNest()
       
    InImage = self:AddInput("Input", "Input", {
        LINKID_DataType = "Image",
        LINK_Main = 1,
    })

    OutImage = self:AddOutput("Output", "Output", {
       LINKID_DataType = "Image",
       LINK_Main = 1,
    })
end
 
function Process(req)
   
    local src = InImage:GetValue(req)
    --local dst = Image({IMG_Like = src})
    local dst = Image{ IMG_Like = src, IMG_DeferAlloc = true }

    if not req:IsPreCalc() then

        ---====  PIXEL PROCESS ===---
       
        --This calls on our kernel to process the image we created.
        local node = DVIPComputeNode(req, "SolidTIHSVKernel", SolidTIHSVKernel, "SolidTIHSVParams", SolidTIHSVParams)
     
        local params = node:GetParamBlock(SolidTIHSVParams)
        --This gets the values of our sliders from the control panel.
        params.blk = InBl:GetValue(req).Value

        params.wht = InW:GetValue(req).Value

        params.red[0] = InRH:GetValue(req).Value
        params.red[1] = InRS:GetValue(req).Value
        params.red[2] = InRV:GetValue(req).Value

        params.grn[0] = InGH:GetValue(req).Value
        params.grn[1] = InGS:GetValue(req).Value
        params.grn[2] = InGV:GetValue(req).Value

        params.blu[0] = InBH:GetValue(req).Value
        params.blu[1] = InBS:GetValue(req).Value
        params.blu[2] = InBV:GetValue(req).Value

        params.cyn[0] = InCH:GetValue(req).Value
        params.cyn[1] = InCS:GetValue(req).Value
        params.cyn[2] = InCV:GetValue(req).Value

        params.mag[0] = InMH:GetValue(req).Value
        params.mag[1] = InMS:GetValue(req).Value
        params.mag[2] = InMV:GetValue(req).Value

        params.yel[0] = InYH:GetValue(req).Value
        params.yel[1] = InYS:GetValue(req).Value
        params.yel[2] = InYV:GetValue(req).Value

        params.srcCompOrder = src:IsMask() and 1 or 15
     
        node:SetParamBlock(params)
     
        node:AddInput("src", src)
        node:AddOutput("dst", dst)
     
        local ok = node:RunSession(req)
     
        if not ok then
            dst = nil
        end

    end
 
    OutImage:Set(req, dst)
end

--These are the parameters that we need access to in our kernel.
SolidTIHSVParams = [[
    int srcCompOrder;
    float blk;
    float wht;
    float red[3];
    float grn[3];
    float blu[3];
    float cyn[3];
    float mag[3];
    float yel[3];
]]
 
--This is the GPU kernel, all of the image algorithms happen here.
SolidTIHSVKernel = [[
    #define blk params->blk

    #define wht params->wht

    #define r_Hue params->red[0]
    #define r_Sat params->red[1]
    #define r_Val params->red[2]

    #define g_Hue params->grn[0]
    #define g_Sat params->grn[1]
    #define g_Val params->grn[2]

    #define b_Hue params->blu[0]
    #define b_Sat params->blu[1]
    #define b_Val params->blu[2]

    #define c_Hue params->cyn[0]
    #define c_Sat params->cyn[1]
    #define c_Val params->cyn[2]

    #define m_Hue params->mag[0]
    #define m_Sat params->mag[1]
    #define m_Val params->mag[2]

    #define y_Hue params->yel[0]
    #define y_Sat params->yel[1]
    #define y_Val params->yel[2]

    #define make_float3 to_float3

    __KERNEL__ void SolidTIHSVKernel(
        __CONSTANTREF__ SolidTIHSVParams *params,
        __TEXTURE2D__ src,
        __TEXTURE2D_WRITE__ dst
    )
    {
        DEFINE_KERNEL_ITERATORS_XY(x, y);
        float4 In = _tex2DVecN(src, x, y, params->srcCompOrder);
        float3 rgb;

        const float r = In.x;
        const float g = In.y;
        const float b = In.z;

        float3 red = make_float3(r_Val + 1.0f, r_Val - r_Sat, r_Val + r_Hue - r_Sat); 
        float3 grn = make_float3(g_Val - g_Sat, g_Val + 1.0f, g_Val + g_Hue - g_Sat);
        float3 blu = make_float3(b_Val + b_Hue - b_Sat, b_Val - b_Sat, b_Val + 1.0f);
        float3 cyn = make_float3(c_Val - c_Sat, c_Val + 1.0f + c_Hue, c_Val + 1.0f);
        float3 mag = make_float3(m_Val + 1.0f, m_Val - m_Sat, m_Val + 1.0f + m_Hue);
        float3 yel = make_float3(y_Val + 1.0f + y_Hue, y_Val + 1.0f, y_Val - y_Sat);
 
        if (r>g) {
            // r>g>b
            if (g>b) {
                rgb = r*(red-blk)+blk + g*(yel-red) + b*(wht-yel);
            }
            // r>b>g
            else if (r>b) {
                rgb = r*(red-blk)+blk + g*(wht-mag) + b*(mag-red);
            }
            // b>r>g
            else {
                rgb = r*(mag-blu) + g*(wht-mag) + b*(blu-blk)+blk;
            }
        } else {
            // b>g>r
            if (b>g) {
                rgb = r*(wht-cyn) + g*(cyn-blu) + b*(blu-blk)+blk;
            }
            // g>b>r
            else if (b>r) {
                rgb = r*(wht-cyn) + g*(grn-blk)+blk + b*(cyn-grn);
            }
            // g>r>b
            else {
                rgb = r*(yel-grn) + g*(grn-blk)+blk + b*(wht-yel);
            }
        }

        _tex2DVec4Write(dst, x, y, to_float4(rgb.x, rgb.y, rgb.z, In.w));
    }
]]