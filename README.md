!
function(e) {
    function n(o) {
        if (t[o]) return t[o].exports;
        var r = t[o] = {
            i: o,
            l: !1,
            exports: {}
        };
        return e[o].call(r.exports, r, r.exports, n),
        r.l = !0,
        r.exports
    }
    var t = {};
    n.m = e,
    n.c = t,
    n.i = function(e) {
        return e
    },
    n.d = function(e, t, o) {
        n.o(e, t) || Object.defineProperty(e, t, {
            configurable: !1,
            enumerable: !0,
            get: o
        })
    },
    n.n = function(e) {
        var t = e && e.__esModule ?
        function() {
            return e.
        default
        }:
        function() {
            return e
        };
        return n.d(t, "a", t),
        t
    },
    n.o = function(e, n) {
        return Object.prototype.hasOwnProperty.call(e, n)
    },
    n.p = "https://ae.bdstatic.com/xz/msite/static/sdk/",
    n(n.s = 35)
} ({
    1 : function(e, n, t) {
        "use strict";
        function o() {
            return y
        }
        function r() {
            document.write('<div id="cambrian-document-write-test"></div>');
            var e = document.getElementById("cambrian-document-write-test");
            return !! e && (e.parentNode.removeChild(e), !0)
        }
        function i(e) {
            var n = arguments.length > 1 && void 0 !== arguments[1] ? arguments[1] : v,
            t = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : v;
            r() ? (window[_].logData.mlt = 1, c(e, n,
            function() {
                a(e, n, t)
            })) : (window[_].logData.mlt = 0, a(e, n, t))
        }
        function a(e) {
            var n = arguments.length > 1 && void 0 !== arguments[1] ? arguments[1] : v,
            t = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : v,
            o = document.createElement("script");
            o.onload = n,
            o.onerror = t,
            o.src = e,
            document.head.appendChild(o)
        }
        function c(e) {
            var n = arguments.length > 1 && void 0 !== arguments[1] ? arguments[1] : v,
            t = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : v,
            o = parseInt(1e3 * Math.random(), 10),
            r = "cambrian_sync_loader_success" + +new Date + o,
            i = "cambrian_sync_loader_fail_" + +new Date + o;
            window[r] = function() {
                delete window[r],
                delete window[i],
                n()
            },
            window[i] = function() {
                delete window[r],
                delete window[i],
                t()
            };
            var a = "<script onload=\"window['" + r + "']()\" onerror=\"window['" + i + '\']()" src="' + e + '"><\/script>';
            document.write(a)
        }
        function d() {
            var e = w[b]("head")[0],
            n = w[g]("style");
            n.innerHTML = "\n        #cambrian0,\n        #cambrian1,\n        #cambrian2,\n        #cambrian3,\n        #cambrian4 {\n            height: 58px;\n        }\n    ",
            e.appendChild(n)
        }
        function s(e, n) {
            var t = void 0,
            o = n;
            o || (t = w[b]("script"), o = t[t.length - 1]);
            var r = w[g]("div");
            return r.id = C + I++,
            r.barType = e,
            o.parentNode.insertBefore(r, o),
            r
        }
        function u(e) {
            var n = Object.keys(e),
            t = n.map(function(n) {
                return n + "=" + encodeURIComponent(e[n])
            }),
            o = t.join("&"),
            r = O + "?" + o; (new Image).src = r
        }
        function l(e) {
            u(p({},
            e, {
                pid: 66,
                sub_pid: 1,
                log_type: 1,
                s_type: "ab",
                ver: "0.0.5",
                pt: "online"
            }))
        }
        function f() {
            for (var e = [], n = "0123456789abcdef", t = 0; t < 36; t++) e[t] = n.substr(Math.floor(16 * Math.random()), 1);
            return e.join("")
        }
        function m(e, n, t) {
            e.style.height = n,
            e.style.margin = t
        }
        function h() {
            I = 0
        }
        Object.defineProperty(n, "__esModule", {
            value: !0
        });
        var p = Object.assign ||
        function(e) {
            for (var n = 1; n < arguments.length; n++) {
                var t = arguments[n];
                for (var o in t) Object.prototype.hasOwnProperty.call(t, o) && (e[o] = t[o])
            }
            return e
        };
        n.getProtocol = o,
        n.detectDocWrite = r,
        n.loadJS = i,
        n.asyncLoader = a,
        n.syncLoader = c,
        n.createStyle = d,
        n.createDom = s,
        n.abLog = l,
        n.uuid = f,
        n.setPlaceHolder = m,
        n.clearCnt = h;
        var v = function() {},
        w = document,
        b = "getElementsByTagName",
        g = "createElement",
        y = "https:",
        _ = "cambrian4706980a",
        O = "https://xiongzhang.baidu.com/xzhstatistics/rp",
        I = 0,
        C = "cambrian"
    },
    2 : function(e, n, t) {
        "use strict";
        function o(e, n) {
            if (! (e instanceof n)) throw new TypeError("Cannot call a class as a function")
        }
        Object.defineProperty(n, "__esModule", {
            value: !0
        }),
        n.Invoker = function e(n) {
            var t = arguments.length > 1 && void 0 !== arguments[1] ? arguments[1] : {};
            o(this, e),
            this.name = n,
            this.options = t;
            for (var r = arguments.length,
            i = Array(r > 2 ? r - 2 : 0), a = 2; a < r; a++) i[a - 2] = arguments[a];
            this.ext = i
        }
    },
    35 : function(e, n, t) {
        "use strict";
        var o = t(2),
        r = t(1),
        i = window.cambrian = {},
        a = window["cambrian4706980a"] = {
            invokerCache: [],
            data: JSON.parse('"{"office_info":{"appid":1598694204208802,"pa_uid":17592191739187,"name":"\u662d\u901a\u6b27\u4e9a","avatar":"https:\/\/cambrian-images.cdn.bcebos.com\/4e79a3467ed2c2669e8c41510209161b_1524633217881.jpeg","description":"\u5173\u7231\u7537\u6027\u5065\u5eb7\uff0c\u4f20\u64ad\u79d1\u5b66\u4e24\u6027\u77e5\u8bc6\u3002"},"client_id":"","homepage":"https:\/\/m.baidu.com\/l=1\/tc?sec=31061&di=e14b04fe7b3b42d4&bdenc=1&nsrc=IlPT2AEptyoA_yixCFOxCGZb8c3JV3T5ABOIQSZLAHSwnESzbbrgHtkfEFX8L8KTZpPPdTPXqRc1xHKb_7Qm9Rp0rrdnpTthlCDwdsigxdLXWM2yrc1k0tPWSSkoyLm&lid=2271609831&clk_extra=%7B%22a%22%3A1598694204208802%7D","login":1,"subscribe":0,"abilities":["isSubscribe","render","bar","isBox","isIos","isAndroid","boxVersion","boxVersionCompare","init","destory","authorize"],"schemes":[],"timestamp":0,"nonce_str":null,"url":null,"signature":null,"bdstoken":"6d580d810472dbcb2bb00b58dd2357e4","tp_id":0,"tp_client_id":null,"auth_token":null,"auth_result":{"code":306000,"msg":"\u7f3a\u5931\u53c2\u6570: timestamp"}}'.substr(1)),
            logData: {
                cs: (new Date).getTime()
            },
            code: "0"
        };
        if (a.code - 0) throw "\u51fa\u9519\u4e86\uff0c\u9519\u8befid: 0, \u9519\u8bef\u4fe1\u606f: "; ["getInfo", "subscribe", "bar", "render", "isSubscribe", "isBox", "isIos", "isAndroid", "boxVersion", "boxVersionCompare", "invokeIM", "follow", "wysFollow", "query", "share", "authorize", "init", "destory", "login", "isLogin", "tel", "sms"].forEach(function(e) {
            i[e] = function() {
                var n = arguments.length > 0 && void 0 !== arguments[0] ? arguments[0] : {},
                t = arguments[1];
                "render" === e && (n = {
                    data: {
                        type: n,
                        anchor: t
                    }
                }),
                n.log = {
                    name: e,
                    ct: (new Date).getTime(),
                    pt: "online",
                    cltype: 0
                },
                a.invokerCache.push(new o.Invoker(e, n))
            }
        }),
        (0, r.loadJS)("https://ae.bdstatic.com/xz/msite/static/sdk/main.f71b4fc1.js")
    }
});
