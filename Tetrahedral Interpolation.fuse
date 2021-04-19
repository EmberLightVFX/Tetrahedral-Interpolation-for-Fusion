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

FuRegisterClass("TetrahedralInterpolation", CT_Tool, {
    REGS_Name = "Tetrahedral Interpolation",
    REGS_Category = "Color",
    REGS_OpIconString = "TI",
    REGS_OpDescription = "",
    REGS_Company = "Ember Light",
    REG_Fuse_NoEdit = false,
    REG_Fuse_NoReload = false,
    REG_SupportsDoD = false,
})

function Create()
    --BLACK
    self:BeginControlNest("Black", "BLACK", true, {})   
    InBlR = self:AddInput(" ", "BlR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 9,
    })

    InBlG = self:AddInput("BlG", "BlG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 9,
    })

    InBlB = self:AddInput("BlB", "BlB", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 9,
    })
    self:EndControlNest()

    --WHITE
    self:BeginControlNest("White", "WHITE", true, {})   
    InWR = self:AddInput(" ", "WR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 8,
    })

    InWG = self:AddInput("WG", "WG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 8,
    })

    InWB = self:AddInput("WB", "WB", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 8,
    })
    self:EndControlNest()

    --RED
    self:BeginControlNest("Red", "RED", true, {})   
    InRR = self:AddInput(" ", "RR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 2,
    })

    InRG = self:AddInput("RG", "RG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 2,
    })

    InRB = self:AddInput("RB", "RB", {
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
    InGR = self:AddInput(" ", "GR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        LINKS_Name = "Green",
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 3,
    })

    InGG = self:AddInput("GG", "GG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 3,
    })

    InGB = self:AddInput("GB", "GB", {
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
    InBR = self:AddInput(" ", "BR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        LINKS_Name = "Blue",
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 4,
    })

    InBG = self:AddInput("BG", "BG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 4,
    })

    InBB = self:AddInput("BB", "BB", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 4,
    })
    self:EndControlNest()

    --Cyan
    self:BeginControlNest("Cyan", "CYAN", true, {}) 
    InCR = self:AddInput(" ", "CR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        LINKS_Name = "Cyan",
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 5,
    })

    InCG = self:AddInput("CG", "CG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 5,
    })

    InCB = self:AddInput("CB", "CB", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 5,
    })
    self:EndControlNest()

    --Magenta
    self:BeginControlNest("Magenta", "MAGENTA", true, {})   
    InMR = self:AddInput(" ", "MR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        LINKS_Name = "Magenta",
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 6,
    })

    InMG = self:AddInput("MG", "MG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 0,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 6,
    })

    InMB = self:AddInput("MB", "MB", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 2,
        IC_ControlGroup = 6,
    })
    self:EndControlNest()

    --Yellow
    self:BeginControlNest("Yellow", "YELLOW", true, {}) 
    InYR = self:AddInput(" ", "YR", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        LINKS_Name = "Yellow",
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 0,
        IC_ControlGroup = 7,
    })

    InYG = self:AddInput("YG", "YG", {
        INP_MinScale = -1,
        INP_MaxScale = 1,
        INP_Default = 1,
        INPID_InputControl = "ColorControl",
        CLRC_ColorSpace = 0,
        LINKID_DataType = "Number",
        IC_ControlID = 1,
        IC_ControlGroup = 7,
    })

    InYB = self:AddInput("YB", "YB", {
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
        local node = DVIPComputeNode(req, "SolidTIKernel", SolidTIKernel, "SolidTIParams", SolidTIParams)
     
        local params = node:GetParamBlock(SolidTIParams)
        --This gets the values of our sliders from the control panel.
        params.blk[0] = InBlR:GetValue(req).Value
        params.blk[1] = InBlG:GetValue(req).Value
        params.blk[2] = InBlB:GetValue(req).Value

        params.wht[0] = InWR:GetValue(req).Value
        params.wht[1] = InWG:GetValue(req).Value
        params.wht[2] = InWB:GetValue(req).Value

        params.red[0] = InRR:GetValue(req).Value
        params.red[1] = InRG:GetValue(req).Value
        params.red[2] = InRB:GetValue(req).Value

        params.grn[0] = InGR:GetValue(req).Value
        params.grn[1] = InGG:GetValue(req).Value
        params.grn[2] = InGB:GetValue(req).Value

        params.blu[0] = InBR:GetValue(req).Value
        params.blu[1] = InBG:GetValue(req).Value
        params.blu[2] = InBB:GetValue(req).Value

        params.cyn[0] = InCR:GetValue(req).Value
        params.cyn[1] = InCG:GetValue(req).Value
        params.cyn[2] = InCB:GetValue(req).Value

        params.mag[0] = InMR:GetValue(req).Value
        params.mag[1] = InMG:GetValue(req).Value
        params.mag[2] = InMB:GetValue(req).Value

        params.yel[0] = InYR:GetValue(req).Value
        params.yel[1] = InYG:GetValue(req).Value
        params.yel[2] = InYB:GetValue(req).Value

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
SolidTIParams = [[
    int srcCompOrder;
    float blk[3];
    float wht[3];
    float red[3];
    float grn[3];
    float blu[3];
    float cyn[3];
    float mag[3];
    float yel[3];
]]
 
--This is the GPU kernel, all of the image algorithms happen here.
SolidTIKernel = [[
    #define bl_R params->blk[0]
    #define bl_G params->blk[1]
    #define bl_B params->blk[2]

    #define wh_R params->wht[0]
    #define wh_G params->wht[1]
    #define wh_B params->wht[2]

    #define r_R params->red[0]
    #define r_G params->red[1]
    #define r_B params->red[2]

    #define g_R params->grn[0]
    #define g_G params->grn[1]
    #define g_B params->grn[2]

    #define b_R params->blu[0]
    #define b_G params->blu[1]
    #define b_B params->blu[2]

    #define c_R params->cyn[0]
    #define c_G params->cyn[1]
    #define c_B params->cyn[2]

    #define m_R params->mag[0]
    #define m_G params->mag[1]
    #define m_B params->mag[2]

    #define y_R params->yel[0]
    #define y_G params->yel[1]
    #define y_B params->yel[2]

    #define make_float3 to_float3

    __KERNEL__ void SolidTIKernel(
        __CONSTANTREF__ SolidTIParams *params,
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
        
        float3 blk = make_float3(bl_R, bl_G, bl_B);
        float3 wht = make_float3(wh_R, wh_G, wh_B);
        float3 red = make_float3(r_R, r_G, r_B); 
        float3 grn = make_float3(g_R, g_G, g_B);
        float3 blu = make_float3(b_R, b_G, b_B);
        float3 cyn = make_float3(c_R, c_G, c_B);
        float3 mag = make_float3(m_R, m_G, m_B);
        float3 yel = make_float3(y_R, y_G, y_B);


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