/*
 * ╔══════════════════════════════════════════════════════════════════════╗
 * ║  GITHUB // AURORA SLATE                                              ║
 * ║  Glassmorphic • Emerald • Cyber Violet • Warm Amber                  ║
 * ║                                                                      ║
 * ║  Compatible with: Stylus / Stylish / UserCSS                        ║
 * ║  Recommended: GitHub Dark mode                                       ║
 * ╚══════════════════════════════════════════════════════════════════════╝
 *
 *  Design tokens
 *  ─────────────────────────────────────────────────────────────────────
 */

:root {
  --aurora-bg: #0b0f19;
  --aurora-bg-deep: #080c14;
  --aurora-surface: rgba(18, 24, 38, 0.75);
  --aurora-surface-solid: #121826;
  --aurora-surface-hover: rgba(24, 32, 50, 0.88);

  --aurora-border: rgba(255, 255, 255, 0.08);
  --aurora-border-bright: rgba(255, 255, 255, 0.14);

  --aurora-emerald: #00f5a0;
  --aurora-emerald-soft: rgba(0, 245, 160, 0.16);
  --aurora-emerald-glow: rgba(0, 245, 160, 0.30);

  --aurora-violet: #7b2cbf;
  --aurora-violet-bright: #a855f7;
  --aurora-violet-soft: rgba(123, 44, 191, 0.18);

  --aurora-amber: #ffb703;
  --aurora-amber-soft: rgba(255, 183, 3, 0.16);

  --aurora-text: #edf2f7;
  --aurora-text-muted: #8d99ae;
  --aurora-text-dim: #667085;

  --aurora-radius: 12px;
  --aurora-radius-sm: 9px;
  --aurora-pill: 999px;

  --aurora-shadow:
    0 12px 40px rgba(0, 0, 0, 0.28);

  --aurora-glow:
    0 0 24px rgba(0, 245, 160, 0.08);

  --aurora-transition:
    all 0.2s cubic-bezier(0.2, 0.8, 0.2, 1);

  --aurora-code:
    "JetBrains Mono", "Fira Code", "SFMono-Regular",
    Consolas, "Liberation Mono", monospace;

  --aurora-sans:
    Inter, -apple-system, BlinkMacSystemFont, "Segoe UI",
    Helvetica, Arial, sans-serif;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  GLOBAL CANVAS
 * ═══════════════════════════════════════════════════════════════════════
 */

html,
body {
  background:
    radial-gradient(
      900px 600px at 0% 0%,
      rgba(123, 44, 191, 0.13),
      transparent 62%
    ),
    radial-gradient(
      850px 600px at 100% 0%,
      rgba(0, 245, 160, 0.08),
      transparent 60%
    ),
    var(--aurora-bg) !important;

  color: var(--aurora-text) !important;
  font-family: var(--aurora-sans) !important;
}

body {
  min-height: 100vh;
}

* {
  scrollbar-width: thin;
  scrollbar-color: rgba(123, 44, 191, 0.65) transparent;
}

*::-webkit-scrollbar {
  width: 6px;
  height: 6px;
}

*::-webkit-scrollbar-track {
  background: transparent;
}

*::-webkit-scrollbar-thumb {
  border-radius: 999px;
  background: linear-gradient(
    180deg,
    rgba(123, 44, 191, 0.75),
    rgba(0, 245, 160, 0.65)
  );
}

*::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(
    180deg,
    var(--aurora-violet-bright),
    var(--aurora-emerald)
  );
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  HEADER / GLOBAL NAVIGATION
 * ═══════════════════════════════════════════════════════════════════════
 */

.Header,
header.Header,
[data-testid="header"] {
  background:
    rgba(11, 15, 25, 0.82) !important;

  backdrop-filter: blur(16px) saturate(130%);
  -webkit-backdrop-filter: blur(16px) saturate(130%);

  border-bottom:
    1px solid var(--aurora-border) !important;

  box-shadow:
    0 8px 30px rgba(0, 0, 0, 0.18);

  position: relative;
  z-index: 100;
}

.Header-link,
.Header-item,
.Header-nav-link {
  color: var(--aurora-text-muted) !important;
  transition: var(--aurora-transition);
}

.Header-link:hover,
.Header-nav-link:hover {
  color: var(--aurora-emerald) !important;
}


/*
 * GitHub logo
 */

.octicon-mark-github,
.Header-link .octicon {
  transition: var(--aurora-transition);
}

.Header-link:hover .octicon-mark-github {
  color: var(--aurora-emerald);
  filter:
    drop-shadow(0 0 8px rgba(0, 245, 160, 0.5));
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  GLOBAL LINKS
 * ═══════════════════════════════════════════════════════════════════════
 */

a {
  color: #b9c5d6;
  transition: color 0.18s ease, text-shadow 0.18s ease;
}

a:hover {
  color: var(--aurora-emerald);
  text-decoration: none;
}

.Link--primary,
.Link--secondary {
  color: inherit;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  GLASS COMPONENT SYSTEM
 * ═══════════════════════════════════════════════════════════════════════
 */

.Box,
.box,
.border,
.BorderGrid-cell,
.Box-row,
.Box-header,
.dropdown-menu,
.SelectMenu-modal,
.SelectMenu-list,
.Popover,
.js-notification-shelf,
.notification-shelf,
.repository-content .js-repo-filter,
.js-repo-filter {
  background:
    var(--aurora-surface) !important;

  backdrop-filter: blur(12px) saturate(125%);
  -webkit-backdrop-filter: blur(12px) saturate(125%);

  border-color:
    var(--aurora-border) !important;

  box-shadow:
    var(--aurora-shadow),
    inset 0 1px 0 rgba(255, 255, 255, 0.025);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  CARDS / REPOSITORY ROWS
 * ═══════════════════════════════════════════════════════════════════════
 */

.Box-row,
.repo-list-item,
.repository-content .Box-row,
.js-navigation-item,
.discussion-timeline .timeline-comment {
  border-radius: var(--aurora-radius) !important;
  border: 1px solid var(--aurora-border) !important;
  margin-bottom: 8px;

  transition: var(--aurora-transition);
}

.Box-row:hover,
.repo-list-item:hover,
.repository-content .Box-row:hover,
.js-navigation-item:hover {
  background:
    var(--aurora-surface-hover) !important;

  border-color:
    rgba(0, 245, 160, 0.18) !important;

  transform: translateY(-2px);

  box-shadow:
    0 12px 30px rgba(0, 0, 0, 0.24),
    0 0 22px rgba(0, 245, 160, 0.055);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  REPOSITORY HEADER
 * ═══════════════════════════════════════════════════════════════════════
 */

.pagehead,
.repohead,
.repohead-details,
.repository-content .Box-header {
  background:
    rgba(18, 24, 38, 0.60) !important;

  border-color:
    var(--aurora-border) !important;
}

.repohead h1,
.repohead .author,
.repohead .author a {
  color: var(--aurora-text) !important;
}

.repohead h1 a:hover {
  color: var(--aurora-emerald) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  REPOSITORY NAVIGATION TABS
 * ═══════════════════════════════════════════════════════════════════════
 */

.UnderlineNav,
.UnderlineNav-body {
  background: transparent !important;
  border-color: var(--aurora-border) !important;
}

.UnderlineNav-item {
  color: var(--aurora-text-muted) !important;
  border-bottom: 2px solid transparent !important;
  transition: var(--aurora-transition);
}

.UnderlineNav-item:hover {
  color: var(--aurora-text) !important;
  border-bottom-color:
    rgba(0, 245, 160, 0.45) !important;
}

.UnderlineNav-item.selected,
.UnderlineNav-item[aria-current="page"] {
  color: var(--aurora-emerald) !important;
  border-bottom-color:
    var(--aurora-emerald) !important;

  text-shadow:
    0 0 12px rgba(0, 245, 160, 0.35);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  BUTTONS
 * ═══════════════════════════════════════════════════════════════════════
 */

.btn,
.Button,
button,
input[type="submit"] {
  border-radius: var(--aurora-pill) !important;

  border-color:
    var(--aurora-border-bright) !important;

  background:
    rgba(24, 32, 50, 0.78) !important;

  color: var(--aurora-text) !important;

  transition: var(--aurora-transition);
}

.btn:hover,
.Button:hover,
button:hover {
  background:
    rgba(35, 45, 67, 0.92) !important;

  border-color:
    rgba(0, 245, 160, 0.28) !important;

  transform: translateY(-1px);

  box-shadow:
    0 5px 18px rgba(0, 0, 0, 0.20),
    0 0 16px rgba(0, 245, 160, 0.08);
}


/*
 * Primary CTA
 */

.btn-primary,
.Button--primary,
button[data-color="accent"] {
  background:
    linear-gradient(
      135deg,
      #00d98f,
      var(--aurora-emerald)
    ) !important;

  color: #06120e !important;

  border-color:
    rgba(0, 245, 160, 0.8) !important;

  font-weight: 700;

  box-shadow:
    0 0 18px rgba(0, 245, 160, 0.12);
}

.btn-primary:hover,
.Button--primary:hover {
  background:
    linear-gradient(
      135deg,
      var(--aurora-emerald),
      #35ffc0
    ) !important;

  color: #03100b !important;

  box-shadow:
    0 0 25px rgba(0, 245, 160, 0.28);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  INPUTS / SEARCH
 * ═══════════════════════════════════════════════════════════════════════
 */

.form-control,
.form-select,
.input,
input,
textarea,
select,
.header-search-input,
.search-input {
  background:
    rgba(9, 14, 24, 0.72) !important;

  color: var(--aurora-text) !important;

  border:
    1px solid var(--aurora-border-bright) !important;

  border-radius:
    var(--aurora-pill) !important;

  transition: var(--aurora-transition);
}

textarea {
  border-radius: var(--aurora-radius) !important;
}

.form-control:focus,
.form-select:focus,
.input:focus,
input:focus,
textarea:focus,
select:focus {
  border-color:
    rgba(0, 245, 160, 0.60) !important;

  outline: none !important;

  box-shadow:
    0 0 0 3px rgba(0, 245, 160, 0.08),
    0 0 18px rgba(0, 245, 160, 0.18) !important;
}

::placeholder {
  color: var(--aurora-text-dim) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  DROPDOWNS / MENUS
 * ═══════════════════════════════════════════════════════════════════════
 */

.dropdown-menu,
.SelectMenu-modal,
[role="menu"],
[role="listbox"] {
  background:
    rgba(18, 24, 38, 0.90) !important;

  backdrop-filter: blur(18px) saturate(140%);
  -webkit-backdrop-filter: blur(18px) saturate(140%);

  border:
    1px solid var(--aurora-border-bright) !important;

  border-radius:
    var(--aurora-radius) !important;

  box-shadow:
    0 20px 60px rgba(0, 0, 0, 0.42),
    0 0 30px rgba(123, 44, 191, 0.06);
}

.dropdown-item,
.SelectMenu-item,
[role="menuitem"],
[role="option"] {
  color: var(--aurora-text-muted) !important;
  border-radius: 8px;
  margin: 2px 5px;
  transition: var(--aurora-transition);
}

.dropdown-item:hover,
.SelectMenu-item:hover,
.SelectMenu-item[aria-selected="true"],
[role="menuitem"]:hover,
[role="option"]:hover {
  background:
    rgba(0, 245, 160, 0.08) !important;

  color:
    var(--aurora-emerald) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  LABELS / TOPICS / TAGS
 * ═══════════════════════════════════════════════════════════════════════
 */

.Label,
.IssueLabel,
.topic-tag,
.repository-meta .topic-tag,
.Label--secondary {
  border-radius:
    var(--aurora-pill) !important;

  background:
    var(--aurora-violet-soft) !important;

  color:
    #c084fc !important;

  border:
    1px solid rgba(168, 85, 247, 0.22) !important;
}

.Label:hover,
.topic-tag:hover {
  background:
    rgba(123, 44, 191, 0.30) !important;

  box-shadow:
    0 0 14px rgba(123, 44, 191, 0.18);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  CODE / COMMITS / HASHES
 * ═══════════════════════════════════════════════════════════════════════
 */

code,
tt,
kbd,
.blob-code,
.blob-code-inner,
.commit-ref,
.commit-ref-name,
.sha,
.commit-sha,
[class*="commit"] code {
  font-family: var(--aurora-code) !important;
}

code,
tt,
kbd {
  color:
    #c084fc !important;

  background:
    rgba(123, 44, 191, 0.13) !important;

  border:
    1px solid rgba(123, 44, 191, 0.16);

  border-radius: 6px;
}

.commit-ref,
.commit-ref-name,
.sha {
  color:
    #b779ff !important;
}


/*
 * Inline highlighted code / diff emphasis
 */

.highlight,
.highlight pre,
.markdown-body mark {
  background:
    rgba(255, 183, 3, 0.10) !important;

  color:
    var(--aurora-amber) !important;
}

.markdown-body code {
  color: #ffc857 !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  MARKDOWN / PROSE
 * ═══════════════════════════════════════════════════════════════════════
 */

.markdown-body {
  color: #c9d2df !important;
}

.markdown-body h1,
.markdown-body h2,
.markdown-body h3,
.markdown-body h4 {
  color: var(--aurora-text) !important;
}

.markdown-body blockquote {
  border-left:
    3px solid var(--aurora-emerald) !important;

  color:
    var(--aurora-text-muted) !important;

  background:
    rgba(0, 245, 160, 0.035);

  border-radius: 0 var(--aurora-radius-sm)
    var(--aurora-radius-sm) 0;
}

.markdown-body hr {
  background:
    var(--aurora-border) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  ISSUES / PULL REQUESTS
 * ═══════════════════════════════════════════════════════════════════════
 */

.js-issue-row,
.js-navigation-item,
.Box-row[data-testid],
.discussion-item,
.discussion-timeline .timeline-comment,
.timeline-comment {
  border-radius:
    var(--aurora-radius) !important;

  border:
    1px solid var(--aurora-border) !important;

  transition:
    var(--aurora-transition);
}

.js-issue-row:hover,
.discussion-item:hover,
.discussion-timeline .timeline-comment:hover {
  background:
    rgba(22, 30, 47, 0.80) !important;

  border-color:
    rgba(0, 245, 160, 0.16) !important;

  transform: translateY(-2px);

  box-shadow:
    0 10px 28px rgba(0, 0, 0, 0.20);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  DISCUSSION TIMELINE
 * ═══════════════════════════════════════════════════════════════════════
 */

.discussion-timeline {
  position: relative;
}

.discussion-timeline::before {
  background:
    linear-gradient(
      180deg,
      rgba(0, 245, 160, 0.35),
      rgba(123, 44, 191, 0.25),
      transparent
    ) !important;
}

.timeline-comment {
  background:
    var(--aurora-surface) !important;

  backdrop-filter: blur(10px);
}

.timeline-comment-header {
  background:
    rgba(255, 255, 255, 0.025) !important;

  border-bottom:
    1px solid var(--aurora-border) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  CONTRIBUTION GRAPH
 * ═══════════════════════════════════════════════════════════════════════
 *
 *  Deep navy → blue-violet → teal → emerald
 */

.ContributionCalendar-day[data-level="0"],
.contrib-calendar .ContributionCalendar-day[data-level="0"] {
  fill: #111827 !important;
  background-color: #111827 !important;
}

.ContributionCalendar-day[data-level="1"],
.contrib-calendar .ContributionCalendar-day[data-level="1"] {
  fill: #123b4a !important;
  background-color: #123b4a !important;
}

.ContributionCalendar-day[data-level="2"],
.contrib-calendar .ContributionCalendar-day[data-level="2"] {
  fill: #096b72 !important;
  background-color: #096b72 !important;
}

.ContributionCalendar-day[data-level="3"],
.contrib-calendar .ContributionCalendar-day[data-level="3"] {
  fill: #00a88f !important;
  background-color: #00a88f !important;
}

.ContributionCalendar-day[data-level="4"],
.contrib-calendar .ContributionCalendar-day[data-level="4"] {
  fill: #00f5a0 !important;
  background-color: #00f5a0 !important;

  filter:
    drop-shadow(0 0 4px rgba(0, 245, 160, 0.45));
}


/*
 * Modern GitHub contribution color variables
 */

.ContributionCalendar-grid text,
.contrib-column {
  color: var(--aurora-text-muted) !important;
}

.ContributionCalendar-day {
  stroke: transparent !important;
  rx: 3px;
  ry: 3px;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  PROFILE / SIDEBAR
 * ═══════════════════════════════════════════════════════════════════════
 */

.contrib-column,
.profile-sidebar,
.js-profile-editable-area,
.user-profile-sticky-bar {
  background:
    var(--aurora-surface) !important;

  backdrop-filter:
    blur(12px) saturate(125%);

  border:
    1px solid var(--aurora-border) !important;

  border-radius:
    var(--aurora-radius) !important;

  box-shadow:
    var(--aurora-shadow);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  AVATARS
 * ═══════════════════════════════════════════════════════════════════════
 */

.avatar {
  border:
    1px solid rgba(0, 245, 160, 0.20) !important;

  box-shadow:
    0 0 0 3px rgba(0, 245, 160, 0.025);

  transition: var(--aurora-transition);
}

.avatar:hover {
  border-color:
    rgba(0, 245, 160, 0.55) !important;

  box-shadow:
    0 0 18px rgba(0, 245, 160, 0.18);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  STAR / WATCH / FORK ACTIONS
 * ═══════════════════════════════════════════════════════════════════════
 */

.octicon-star,
[aria-label*="star"] .octicon,
[title*="star"] .octicon {
  color:
    var(--aurora-amber) !important;

  filter:
    drop-shadow(0 0 5px rgba(255, 183, 3, 0.28));
}

.starring-container .octicon-star,
.js-social-container .octicon-star {
  color:
    var(--aurora-amber) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  STATUS INDICATORS
 * ═══════════════════════════════════════════════════════════════════════
 */

.State,
.State--open,
.IssueLabel--opened,
.State--merged {
  border-radius: var(--aurora-pill) !important;
}

.State--open {
  color: var(--aurora-emerald) !important;
  background: var(--aurora-emerald-soft) !important;
  border-color: rgba(0, 245, 160, 0.25) !important;
}

.State--merged {
  color: #c084fc !important;
  background: var(--aurora-violet-soft) !important;
  border-color: rgba(123, 44, 191, 0.30) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  ALERTS / NOTICES
 * ═══════════════════════════════════════════════════════════════════════ */

.flash,
.flash-warn,
.flash-error,
.flash-success {
  border-radius:
    var(--aurora-radius) !important;

  background:
    rgba(18, 24, 38, 0.82) !important;

  backdrop-filter: blur(10px);
}

.flash-success {
  border-color:
    rgba(0, 245, 160, 0.30) !important;

  color:
    var(--aurora-emerald) !important;
}

.flash-warn {
  border-color:
    rgba(255, 183, 3, 0.30) !important;

  color:
    var(--aurora-amber) !important;
}

.flash-error {
  border-color:
    rgba(248, 81, 73, 0.30) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  TABS / FILTER BAR
 * ═══════════════════════════════════════════════════════════════════════
 */

.js-repo-filter,
.repo-list .Box-header,
.filter-bar,
.subnav {
  background:
    rgba(18, 24, 38, 0.68) !important;

  backdrop-filter: blur(12px);

  border:
    1px solid var(--aurora-border) !important;

  border-radius:
    var(--aurora-radius) !important;
}

.filter-item,
.subnav-item {
  border-radius:
    var(--aurora-pill) !important;

  transition: var(--aurora-transition);
}

.filter-item:hover,
.subnav-item:hover {
  background:
    rgba(0, 245, 160, 0.07) !important;

  color:
    var(--aurora-emerald) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  TABLES
 * ═══════════════════════════════════════════════════════════════════════ */

.markdown-body table,
.Box table,
table {
  border-collapse: separate !important;
  border-spacing: 0;
  overflow: hidden;
  border-radius: var(--aurora-radius);
  border: 1px solid var(--aurora-border) !important;
}

.markdown-body table tr,
.Box table tr,
table tr {
  background:
    rgba(18, 24, 38, 0.55) !important;

  border-color:
    var(--aurora-border) !important;
}

.markdown-body table tr:nth-child(2n),
.Box table tr:nth-child(2n),
table tr:nth-child(2n) {
  background:
    rgba(255, 255, 255, 0.018) !important;
}

.markdown-body table th {
  color:
    var(--aurora-emerald) !important;

  background:
    rgba(0, 245, 160, 0.045) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  DIFF VIEW
 * ═══════════════════════════════════════════════════════════════════════ */

.diff-table,
.file,
.js-file-content {
  border-radius:
    var(--aurora-radius) !important;

  overflow: hidden;

  border:
    1px solid var(--aurora-border) !important;
}

.blob-wrapper {
  background:
    rgba(8, 12, 20, 0.72) !important;
}

.blob-code-addition {
  background:
    rgba(0, 245, 160, 0.07) !important;
}

.blob-code-deletion {
  background:
    rgba(255, 70, 70, 0.07) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  TERMINAL / CODE BLOCKS
 * ═══════════════════════════════════════════════════════════════════════ */

.highlight pre,
pre,
.markdown-body pre {
  background:
    #080d17 !important;

  border:
    1px solid var(--aurora-border) !important;

  border-radius:
    var(--aurora-radius) !important;

  box-shadow:
    inset 0 1px 0 rgba(255,255,255,0.025),
    0 12px 35px rgba(0,0,0,0.22);
}

pre code {
  background: transparent !important;
  border: 0 !important;
  color: #c9d2df !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  TOOLTIP
 * ═══════════════════════════════════════════════════════════════════════ */

.tooltipped::after,
[data-tooltip]::after {
  background:
    rgba(18, 24, 38, 0.96) !important;

  color:
    var(--aurora-text) !important;

  border:
    1px solid var(--aurora-border-bright);

  border-radius:
    8px !important;

  box-shadow:
    0 10px 30px rgba(0,0,0,0.30);
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  SELECTED / ACTIVE ELEMENTS
 * ═══════════════════════════════════════════════════════════════════════ */

[aria-current="page"],
[aria-selected="true"],
.selected {
  color:
    var(--aurora-emerald) !important;
}

.form-checkbox input:checked + label::before,
.form-radio input:checked + label::before {
  background-color:
    var(--aurora-emerald) !important;

  border-color:
    var(--aurora-emerald) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  FOCUS ACCESSIBILITY
 * ═══════════════════════════════════════════════════════════════════════ */

:focus-visible {
  outline:
    2px solid rgba(0, 245, 160, 0.65) !important;

  outline-offset: 2px;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  SUBTLE PAGE-LEVEL DEPTH
 * ═══════════════════════════════════════════════════════════════════════ */

main {
  position: relative;
}

main::before {
  content: "";
  position: fixed;
  pointer-events: none;
  z-index: -1;

  inset: 0;

  background:
    radial-gradient(
      600px 400px at 15% 15%,
      rgba(123, 44, 191, 0.045),
      transparent 70%
    ),
    radial-gradient(
      600px 400px at 85% 20%,
      rgba(0, 245, 160, 0.035),
      transparent 70%
    );
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  REDUCE EXCESSIVE GITHUB SHADOWS
 * ═══════════════════════════════════════════════════════════════════════ */

.Box,
.dropdown-menu,
.SelectMenu-modal,
.Popover,
.btn,
.Button {
  box-shadow:
    var(--aurora-shadow) !important;
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  MOBILE POLISH
 * ═══════════════════════════════════════════════════════════════════════ */

@media (max-width: 767px) {
  .Box-row,
  .repo-list-item,
  .timeline-comment,
  .js-issue-row {
    border-radius:
      10px !important;
  }

  .Header {
    backdrop-filter:
      blur(14px) !important;
  }

  .contrib-column {
    border-radius:
      10px !important;
  }
}


/*
 * ═══════════════════════════════════════════════════════════════════════
 *  MOTION SAFETY
 * ═══════════════════════════════════════════════════════════════════════ */

@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    transition-duration: 0.01ms !important;
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
  }
}
