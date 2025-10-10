# Codebase Structure Summary

Total Code Files: 1335
Total Functions: 2221

## Files

### apps\vscode-e2e\src\runTest.ts
**Purpose:** Runs end-to-end tests within a VS Code environment.

**Exported Functions:**
- `main` → `Promise<void>`

**Key Imports:** `path`, `os`, `fs/promises`, `@vscode/test-electron`

---

### apps\vscode-e2e\src\suite\extension.test.ts
**Purpose:** Tests the registration of Roo Code extension commands.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`

**Key Imports:** `assert`, `vscode`, `./test-utils`

---

### apps\vscode-e2e\src\suite\index.ts
**Purpose:** Initializes and runs the Roo Code extension tests.

**Exported Functions:**
- `run` → `Promise<void>`

**Key Imports:** `path`, `mocha`, `glob`, `vscode`, `@roo-code/types`, `./utils`

---

### apps\vscode-e2e\src\suite\markdown-lists.test.ts
**Purpose:** Tests the rendering of markdown lists within the chat interface.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`

**Key Imports:** `assert`, `@roo-code/types`, `./utils`, `./test-utils`

---

### apps\vscode-e2e\src\suite\modes.test.ts
**Purpose:** Verifies correct handling of mode switching in Roo Code.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`

**Key Imports:** `assert`, `@roo-code/types`, `./utils`, `./test-utils`

---

### apps\vscode-e2e\src\suite\subtasks.test.ts
**Purpose:** Tests subtask cancellation and resumption within Roo Code.

**Key Imports:** `assert`, `@roo-code/types`, `./utils`

---

### apps\vscode-e2e\src\suite\task.test.ts
**Purpose:** Tests the correct handling of prompts and responses in tasks.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`

**Key Imports:** `assert`, `@roo-code/types`, `./utils`, `./test-utils`

---

### apps\vscode-e2e\src\suite\test-utils.ts
**Purpose:** Provides utility functions for setting test suite timeouts.

**Exported Functions:**
- `setDefaultSuiteTimeoutcontext: Mocha.Suite` → `void`

**Exported Constants:**
- `DEFAULT_SUITE_TIMEOUT` = `120_000`

---

### apps\vscode-e2e\src\suite\tools\apply-diff.test.ts
**Purpose:** Tests the functionality of the apply_diff tool.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\execute-command.test.ts
**Purpose:** Tests the execute_command tool within the Roo Code extension.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\insert-content.test.ts
**Purpose:** Tests the insert_content tool for inserting content into files.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\list-files.test.ts
**Purpose:** Tests the list_files tool for listing files in a directory.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\read-file.test.ts
**Purpose:** Tests the read_file tool for reading file contents.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `os`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\search-and-replace.test.ts
**Purpose:** Tests the search_and_replace tool's functionality.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\search-files.test.ts
**Purpose:** Tests the search_files tool for finding files by content.

**Exported Functions:**
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\use-mcp-tool.test.ts
**Purpose:** Tests the use_mcp_tool within the Roo Code extension.

**Exported Functions:**
- `skip` → `any`
- `test(name: string, fn: TestFunction)` → `any`
- `suite(name: string, this: ThisType<Mocha.Suite>)` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `os`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\write-to-file.test.ts
**Purpose:** Tests Roo Code's write_to_file tool functionality.

**Exported Functions:**
- `suite(name: string, fn: () => void)` → `void`

**Key Imports:** `assert`, `fs`, `path`, `os`, `@roo-code/types`

---

### apps\vscode-e2e\src\suite\utils.ts
**Purpose:** Provides utility functions for waiting and checking conditions.

**Exported Functions:**
- `waitFor(condition: (() => Promise<boolean>) | (() => boolean), { timeout = 30_000, interval = 250 }: WaitForOptions = {})` → `Promise<void>`
- `waitUntilAborted({ api, taskId, ...options }: WaitUntilAbortedOptions)` → `Promise<void>`
- `waitUntilCompleted({ api, taskId, ...options }: WaitUntilCompletedOptions)` → `Promise<void>`

**Exported Types:**
- `type WaitForOptions`: timeout?: number, interval?: number
- `type WaitUntilAbortedOptions`: api: RooCodeAPI, taskId: string, timeout?: number, interval?: number
- `type WaitUntilCompletedOptions`: api: RooCodeAPI, taskId: string, timeout?: number, interval?: number

**Key Imports:** `@roo-code/types`

---

### apps\vscode-e2e\src\types\global.d.ts
**Purpose:** Declares global variables for the VS Code extension.

**Key Imports:** `@roo-code/types`

---

### apps\web-evals\next-env.d.ts
**Purpose:** Configures Next.js environment types.

---

### apps\web-evals\next.config.ts
**Purpose:** Configures Next.js webpack settings.

**Exported Constants:**
- `nextConfig` = `{}`

**Key Imports:** `next`

---

### apps\web-evals\src\actions\exercises.ts
**Purpose:** Fetches and returns available exercise paths.

**Exported Functions:**
- `getExercises()` → `Promise<string[]>`

**Key Imports:** `path`, `url`, `@roo-code/evals`

---

### apps\web-evals\src\actions\heartbeat.ts
**Purpose:** Retrieves heartbeat data from Redis for a given run ID.

**Exported Functions:**
- `getHeartbeat(runId: number)` → `Promise<string | null>`

**Key Imports:** `@/lib/server/redis`

---

### apps\web-evals\src\actions\runners.ts
**Purpose:** Fetches runner IDs associated with a specific run ID.

**Exported Functions:**
- `getRunners(runId: number)` → `Promise<string[]>`

**Key Imports:** `@/lib/server/redis`

---

### apps\web-evals\src\actions\runs.ts
**Purpose:** Creates and manages evaluation runs based on provided parameters.

**Exported Functions:**
- `createRun({ suite, exercises = [], systemPrompt, timeout, ...values }: CreateRun)` → `Promise<any>`

**Key Imports:** `path`, `fs`, `url`, `next/cache`, `p-map`, `@roo-code/evals`, `@/lib/schemas`

---

### apps\web-evals\src\actions\tasks.ts
**Purpose:** Retrieves tasks associated with a specific run ID.

**Exported Functions:**
- `getTasks(runId: number)` → `Promise<any>`

**Key Imports:** `next/cache`, `@roo-code/evals`

---

### apps\web-evals\src\app\api\health\route.ts
**Purpose:** Provides an API endpoint for health checks.

**Exported Functions:**
- `GET()` → `Promise<NextResponse<any>>`

**Key Imports:** `next/server`

---

### apps\web-evals\src\app\api\runs\[id]\stream\route.ts
**Purpose:** Streams task events for a specific run ID.

**Exported Functions:**
- `GET(request: NextRequest, { params }: { params: Promise<{ id: string }> })` → `Promise<Response>`

**Key Imports:** `next/server`, `@roo-code/types`, `@roo-code/evals`, `@/lib/server/sse-stream`, `@/lib/server/redis`

---

### apps\web-evals\src\app\layout.tsx
**Purpose:** Defines the root layout for the web application.

**Exported Functions:**
- `RootLayout({ children }: Readonly<{ children: React.ReactNode }>)` → `JSX.Element`

**Exported Constants:**
- `metadata` = `{}`

**Key Imports:** `next/font/google`, `@/components/providers`, `@/components/ui`, `@/components/layout/header`

---

### apps\web-evals\src\app\page.tsx
**Purpose:** Renders the home page displaying evaluation runs.

**Exported Functions:**
- `Page()` → `Promise<JSX.Element>`

**Key Imports:** `@roo-code/evals`, `@/components/home/runs`

---

### apps\web-evals\src\app\runs\[id]\page.tsx
**Purpose:** Renders the run details page for a specific ID.

**Exported Functions:**
- `Page({ params }: { params: Promise<{ id: string }> })` → `Promise<JSX.Element>`

**Key Imports:** `@roo-code/evals`, `./run`

---

### apps\web-evals\src\app\runs\[id]\run-status.tsx
**Purpose:** Displays the status of a running evaluation.

**Exported Functions:**
- `RunStatus({ runStatus: { sseStatus, heartbeat, runners = [] } }: { runStatus: _RunStatus })` → `JSX.Element`

**Key Imports:** `react`, `@/hooks/use-run-status`, `@/lib/utils`

---

### apps\web-evals\src\app\runs\[id]\run.tsx
**Purpose:** Renders the detailed view of a specific run.

**Exported Functions:**
- `Run({ run }: { run: Run })` → `JSX.Element`

**Key Imports:** `react`, `lucide-react`, `@roo-code/evals`, `@/lib/formatters`, `@/hooks/use-run-status`, `@/components/ui`

---

### apps\web-evals\src\app\runs\[id]\task-status.tsx
**Purpose:** Renders the status of a task using different Lucide icons.

**Exported Functions:**
- `TaskStatus({ task, running }: TaskStatusProps)` → `JSX.Element`

**Exported Types:**
- `type TaskStatusProps`: task: Task, running: boolean

**Key Imports:** `lucide-react`, `@roo-code/evals`

---

### apps\web-evals\src\app\runs\new\new-run.tsx
**Purpose:** Provides a form for creating new evaluation runs.

**Exported Functions:**
- `NewRun()` → `JSX.Element`

**Key Imports:** `react`, `next/navigation`, `zod`, `@tanstack/react-query`, `react-hook-form`, `sonner`, `lucide-react`, `@roo-code/types`, `@/actions/runs`, `@/actions/exercises`, `@/lib/schemas`, `@/lib/utils`, `@/hooks/use-open-router-models`, `@/components/ui`

---

### apps\web-evals\src\app\runs\new\page.tsx
**Purpose:** Renders the new run creation page.

**Exported Functions:**
- `Page()` → `JSX.Element`

**Key Imports:** `./new-run`

---

### apps\web-evals\src\app\runs\new\settings-diff.tsx
**Purpose:** Displays the differences between default and custom settings.

**Exported Functions:**
- `SettingsDiff({ customSettings: { experiments: customExperiments, ...customSettings }, defaultSettings: { experiments: defaultExperiments, ...defaultSettings }, className, ...props }: SettingsDiffProps)` → `JSX.Element`

**Exported Types:**
- `type SettingsDiffProps`: defaultSettings: RooCodeSettings, customSettings: RooCodeSettings

**Key Imports:** `react`, `@roo-code/types`, `@/lib/utils`

---

### apps\web-evals\src\components\home\run.tsx
**Purpose:** Displays a single evaluation run with actions and metrics.

**Exported Functions:**
- `Run({ run, taskMetrics }: RunProps)` → `JSX.Element`

**Exported Types:**
- `type RunProps`: run: EvalsRun, taskMetrics: EvalsTaskMetrics | null

**Key Imports:** `react`, `next/link`, `lucide-react`, `@roo-code/evals`

---

### apps\web-evals\src\components\home\runs.tsx
**Purpose:** Renders a table displaying a list of evaluation runs.

**Exported Functions:**
- `Runs({ runs }: { runs: RunWithTaskMetrics[] })` → `JSX.Element`

**Exported Types:**
- `type RunWithTaskMetrics`: id: number, model: string, taskMetrics: TaskMetrics | null

**Key Imports:** `next/navigation`, `lucide-react`, `@roo-code/evals`, `@/components/ui`

---

### apps\web-evals\src\components\layout\header.tsx
**Purpose:** Creates the header component for the application layout.

**Exported Functions:**
- `Header()` → `JSX.Element`

**Key Imports:** `./logo`

---

### apps\web-evals\src\components\layout\logo.tsx
**Purpose:** Renders the application logo with hover effects and navigation.

**Exported Functions:**
- `Logo({ width = 50, height = 32, fill = "#fff", className, ...props }: LogoProps)` → `JSX.Element`
- `HoppingLogo()` → `JSX.Element`

**Exported Types:**
- `type LogoProps`: width?: number, height?: number, fill?: string, className?: string

**Key Imports:** `react`, `next/navigation`, `react-use`, `@/lib/utils`

---

### apps\web-evals\src\components\providers\index.ts
**Purpose:** Exports ReactQueryProvider and ThemeProvider components.

---

### apps\web-evals\src\components\providers\react-query-provider.tsx
**Purpose:** Provides React Query functionality to the application.

**Exported Functions:**
- `ReactQueryProvider({ children }: { children: React.ReactNode })` → `JSX.Element`

**Key Imports:** `@tanstack/react-query`

---

### apps\web-evals\src\components\providers\theme-provider.tsx
**Purpose:** Provides theme context using next-themes for the app.

**Exported Functions:**
- `ThemeProvider({ children, ...props }: ThemeProviderProps)` → `JSX.Element`

**Key Imports:** `react`, `next/dynamic`, `next-themes`

---

### apps\web-evals\src\components\ui\alert-dialog.tsx
**Purpose:** Creates an alert dialog component using Radix UI primitives.

**Exported Functions:**
- `AlertDialog({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Root>)` → `JSX.Element`
- `AlertDialogTrigger({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Trigger>)` → `JSX.Element`
- `AlertDialogPortal({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Portal>)` → `JSX.Element`
- `AlertDialogOverlay({ className, ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Overlay>)` → `JSX.Element`
- `AlertDialogContent({ className, ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Content>)` → `JSX.Element`
- `AlertDialogHeader({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Header>)` → `JSX.Element`
- `AlertDialogFooter({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Footer>)` → `JSX.Element`
- `AlertDialogTitle({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Title>)` → `JSX.Element`
- `AlertDialogDescription({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Description>)` → `JSX.Element`
- `AlertDialogAction({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Action>)` → `JSX.Element`
- `AlertDialogCancel({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Cancel>)` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-alert-dialog`, `@/lib/utils`, `@/components/ui/button`

---

### apps\web-evals\src\components\ui\badge.tsx
**Purpose:** Renders a badge component with various styling options.

**Exported Functions:**
- `Badge({ className, variant, asChild = false, ...props }: React.ComponentProps<"span"> & VariantProps<typeof badgeVariants> & { asChild?: boolean })` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-slot`, `class-variance-authority`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\button.tsx
**Purpose:** Creates a button component with various styling options.

**Exported Functions:**
- `Button({ className, variant, size, asChild, ...props }: React.ComponentProps<"button"> & VariantProps<typeof buttonVariants> & { size?: Size; asChild?: boolean })` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-slot`, `class-variance-authority`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\command.tsx
**Purpose:** Implements a command palette UI using cmdk and dialog components.

**Exported Functions:**
- `Command({ className, ...props }: React.ComponentProps<typeof CommandPrimitive>)` → `JSX.Element`
- `CommandDialog({ title = "Command Palette", description = "Search for a command to run...", children, ...props }: React.ComponentProps<typeof Dialog> & { title?: string; description?: string })` → `JSX.Element`
- `CommandInput({ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Input>)` → `JSX.Element`
- `CommandList({ className, ...props }: React.ComponentProps<typeof CommandPrimitive.List>)` → `JSX.Element`
- `CommandEmpty({ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Empty>)` → `JSX.Element`
- `CommandGroup({ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Group>)` → `JSX.Element`
- `CommandSeparator({ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Separator>)` → `JSX.Element`
- `CommandItem({ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Item>)` → `JSX.Element`
- `CommandShortcut({ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Shortcut>)` → `JSX.Element`

**Key Imports:** `react`, `cmdk`, `lucide-react`, `@/lib/utils`, `@/components/ui/dialog`

---

### apps\web-evals\src\components\ui\dialog.tsx
**Purpose:** Creates a dialog component using Radix UI primitives.

**Exported Functions:**
- `Dialog({ ...props }: React.ComponentProps<typeof DialogPrimitive.Root>)` → `JSX.Element`
- `DialogTrigger({ ...props }: React.ComponentProps<typeof DialogPrimitive.Trigger>)` → `JSX.Element`
- `DialogPortal({ ...props }: React.ComponentProps<typeof DialogPrimitive.Portal>)` → `JSX.Element`
- `DialogClose({ ...props }: React.ComponentProps<typeof DialogPrimitive.Close>)` → `JSX.Element`
- `DialogOverlay({ className, ...props }: React.ComponentProps<typeof DialogPrimitive.Overlay>)` → `JSX.Element`
- `DialogContent({ className, children, ...props }: React.ComponentProps<typeof DialogPrimitive.Content>)` → `JSX.Element`
- `DialogHeader({ ...props }: React.ComponentProps<typeof DialogPrimitive.Header>)` → `JSX.Element`
- `DialogFooter({ ...props }: React.ComponentProps<typeof DialogPrimitive.Footer>)` → `JSX.Element`
- `DialogTitle({ ...props }: React.ComponentProps<typeof DialogPrimitive.Title>)` → `JSX.Element`
- `DialogDescription({ ...props }: React.ComponentProps<typeof DialogPrimitive.Description>)` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-dialog`, `lucide-react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\drawer.tsx
**Purpose:** Creates a drawer component using vaul primitives.

**Exported Functions:**
- `Drawer({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Root>)` → `JSX.Element`
- `DrawerTrigger({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Trigger>)` → `JSX.Element`
- `DrawerPortal({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Portal>)` → `JSX.Element`
- `DrawerClose({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Close>)` → `JSX.Element`
- `DrawerOverlay({ className, ...props }: React.ComponentProps<typeof DrawerPrimitive.Overlay>)` → `JSX.Element`
- `DrawerContent({ className, children, ...props }: React.ComponentProps<typeof DrawerPrimitive.Content>)` → `JSX.Element`
- `DrawerHeader({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Header>)` → `JSX.Element`
- `DrawerFooter({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Footer>)` → `JSX.Element`
- `DrawerTitle({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Title>)` → `JSX.Element`
- `DrawerDescription({ ...props }: React.ComponentProps<typeof DrawerPrimitive.Description>)` → `JSX.Element`

**Key Imports:** `react`, `vaul`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\dropdown-menu.tsx
**Purpose:** Creates a dropdown menu component using Radix UI primitives.

**Exported Functions:**
- `DropdownMenu({ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Root>)` → `JSX.Element`
- `DropdownMenuPortal({ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Portal>)` → `JSX.Element`
- `DropdownMenuTrigger({ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Trigger>)` → `JSX.Element`
- `DropdownMenuContent({ className, sideOffset = 4, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Content>)` → `JSX.Element`
- `DropdownMenuGroup({ className, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Group>)` → `JSX.Element`
- `DropdownMenuItem({ className, inset, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Item> & { inset?: boolean })` → `JSX.Element`
- `DropdownMenuCheckboxItem({ className, children, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.CheckboxItem>)` → `JSX.Element`
- `DropdownMenuRadioGroup({ className, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.RadioGroup>)` → `JSX.Element`
- `DropdownMenuRadioItem({ className, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.RadioItem>)` → `JSX.Element`
- `DropdownMenuLabel({ className, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Label>)` → `JSX.Element`
- `DropdownMenuSeparator({ className, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Separator>)` → `JSX.Element`
- `DropdownMenuShortcut({ className, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Shortcut>)` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-dropdown-menu`, `lucide-react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\form.tsx
**Purpose:** Provides form components and utilities using react-hook-form.

**Exported Functions:**
- `FormItem({ className, ...props }: React.HTMLProps<HTMLDivElement>)` → `JSX.Element`
- `FormLabel({ className, ...props }: React.ComponentProps<typeof LabelPrimitive.Root>)` → `JSX.Element`
- `FormControl({ ...props }: React.HTMLProps<HTMLDivElement>)` → `JSX.Element`
- `FormDescription({ className, ...props }: React.HTMLProps<HTMLParagraphElement>)` → `JSX.Element`
- `FormMessage({ className, ...props }: React.HTMLProps<HTMLParagraphElement>)` → `JSX.Element`
- `useFormField()` → `{ id: string; } & { ...; }`

**Exported Types:**
- `type FormFieldContextValue`: name: TName
- `type FormField`: name: TName

**Key Imports:** `react`, `@radix-ui/react-label`, `react-hook-form`, `@/lib/utils`, `@/components/ui/label`

---

### apps\web-evals\src\components\ui\index.ts
**Purpose:** Exports all UI components from the ui directory.

---

### apps\web-evals\src\components\ui\input.tsx
**Purpose:** Creates a styled input component.

**Exported Functions:**
- `Input({ className, type, ...props }: React.ComponentProps<"input">)` → `JSX.Element`

**Key Imports:** `react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\label.tsx
**Purpose:** Creates a styled label component.

**Exported Functions:**
- `Label({ className, ...props }: React.ComponentProps<typeof LabelPrimitive.Root>)` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-label`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\multi-select.tsx
**Purpose:** Creates a multi-select UI component with various styling options.

**Exported Functions:**
- `handleInputKeyDownevent: React.KeyboardEvent<HTMLInputElement>` → `void`
- `toggleOptionvalue: string` → `void`
- `handleTogglePopoveropen: boolean` → `void`
- `clearExtraOptionsevent: React.MouseEvent<HTMLButtonElement, MouseEvent>` → `void`
- `onSelectAllevent: React.MouseEvent<HTMLButtonElement, MouseEvent>` → `void`

**Exported Types:**
- `interface MultiSelectProps`: options: { label: string; value: any }[], onChange?: (value: string[]) => void, value?: string[], placeholder?: string, disabled?: boolean

**Key Imports:** `react`, `class-variance-authority`, `fuzzysort`, `lucide-react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\popover.tsx
**Purpose:** Provides a reusable Popover component using Radix UI primitives.

**Exported Functions:**
- `Popover{ ...props }: React.ComponentProps<typeof PopoverPrimitive.Root>` → `any`
- `PopoverTrigger{ ...props }: React.ComponentProps<typeof PopoverPrimitive.Trigger>` → `any`
- `PopoverContent{ className, align, sideOffset, ...props }: React.ComponentProps<typeof PopoverPrimitive.Content>` → `any`
- `PopoverAnchor{ ...props }: React.ComponentProps<typeof PopoverPrimitive.Anchor>` → `any`

**Key Imports:** `react`, `@radix-ui/react-popover`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\scroll-area.tsx
**Purpose:** Implements a custom scrollable area component with Radix primitives.

**Exported Functions:**
- `ScrollArea{ className, children, viewportRef, ...props }: ScrollAreaProps` → `any`
- `ScrollBar{ className, orientation, ...props }: React.ComponentProps<typeof ScrollAreaPrimitive.ScrollAreaScrollbar>` → `any`

**Exported Types:**
- `type ScrollAreaProps`: viewportRef?: React.RefObject<HTMLDivElement>

**Key Imports:** `react`, `@radix-ui/react-scroll-area`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\select.tsx
**Purpose:** Creates a customizable select component using Radix UI primitives.

**Exported Functions:**
- `Select{ ...props }: React.ComponentProps<typeof SelectPrimitive.Root>` → `any`
- `SelectGroup{ ...props }: React.ComponentProps<typeof SelectPrimitive.Group>` → `any`
- `SelectValue{ ...props }: React.ComponentProps<typeof SelectPrimitive.Value>` → `any`
- `SelectTrigger{ className, size, children, ...props }: React.ComponentProps<typeof SelectPrimitive.Trigger> & { size?: "sm" | "default" }` → `any`
- `SelectContent{ className, children, position, ...props }: React.ComponentProps<typeof SelectPrimitive.Content>` → `any`
- `SelectLabel{ ...props }: React.ComponentProps<typeof SelectPrimitive.Label>` → `any`
- `SelectItem{ children, className, ...props }: React.ComponentProps<typeof SelectPrimitive.Item>` → `any`
- `SelectSeparator{ ...props }: React.ComponentProps<typeof SelectPrimitive.Separator>` → `any`
- `SelectScrollUpButton{ ...props }: React.ComponentProps<typeof SelectPrimitive.ScrollUpButton>` → `any`
- `SelectScrollDownButton{ ...props }: React.ComponentProps<typeof SelectPrimitive.ScrollDownButton>` → `any`

**Key Imports:** `react`, `@radix-ui/react-select`, `lucide-react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\separator.tsx
**Purpose:** Provides a separator component for visual separation in layouts.

**Exported Functions:**
- `Separator{ className, orientation, decorative, ...props }: React.ComponentProps<typeof SeparatorPrimitive.Root>` → `any`

**Key Imports:** `react`, `@radix-ui/react-separator`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\slider.tsx
**Purpose:** Implements a slider component using Radix UI primitives.

**Exported Functions:**
- `Slider{ className, defaultValue, value, min, max, ...props }: React.ComponentProps<typeof SliderPrimitive.Root>` → `any`

**Key Imports:** `react`, `@radix-ui/react-slider`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\sonner.tsx
**Purpose:** Wraps the Sonner Toaster component for theming and styling.

**Exported Functions:**
- `Toaster{ ...props }: ToasterProps` → `any`

**Key Imports:** `next-themes`, `sonner`

---

### apps\web-evals\src\components\ui\table.tsx
**Purpose:** Provides table components for displaying tabular data.

**Exported Functions:**
- `Table{ className, ...props }: React.ComponentProps<"table">` → `any`
- `TableHeader{ className, ...props }: React.ComponentProps<"thead">` → `any`
- `TableBody{ className, ...props }: React.ComponentProps<"tbody">` → `any`
- `TableFooter{ className, ...props }: React.ComponentProps<"tfoot">` → `any`
- `TableRow{ className, ...props }: React.ComponentProps<"tr">` → `any`
- `TableHead{ className, ...props }: React.ComponentProps<"th">` → `any`
- `TableCell{ className, ...props }: React.ComponentProps<"td">` → `any`
- `TableCaption{ className, ...props }: React.ComponentProps<"caption">` → `any`

**Key Imports:** `react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\tabs.tsx
**Purpose:** Creates a tab component using Radix UI primitives.

**Exported Types:**
- `type Tabs`

**Key Imports:** `react`, `useEffect`, `useRef`, `useState`, `@radix-ui/react-tabs`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\textarea.tsx
**Purpose:** Provides a styled textarea component with common UI features.

**Exported Functions:**
- `Textarea{ className, ...props }: React.ComponentProps<"textarea">` → `any`

**Key Imports:** `react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\tooltip.tsx
**Purpose:** Implements a tooltip component using Radix UI primitives.

**Exported Functions:**
- `TooltipProvider{ delayDuration, ...props }: React.ComponentProps<typeof TooltipPrimitive.Provider>` → `any`
- `Tooltip{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Root>` → `any`
- `TooltipTrigger{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Trigger>` → `any`
- `TooltipContent{ className, sideOffset, children, ...props }: React.ComponentProps<typeof TooltipPrimitive.Content>` → `any`

**Key Imports:** `react`, `@radix-ui/react-tooltip`, `@/lib/utils`

---

### apps\web-evals\src\hooks\use-copy-run.ts
**Purpose:** Provides a hook to copy a run to production and display feedback.

**Exported Functions:**
- `useCopyRunrunId: number` → `{ isPending: boolean; copyRun: any; copied: boolean; }`

**Key Imports:** `react`, `@tanstack/react-query`, `sonner`, `@/lib/actions`

---

### apps\web-evals\src\hooks\use-event-source.ts
**Purpose:** Manages an EventSource connection for real-time updates.

**Exported Functions:**
- `useEventSource{ url, withCredentials, onMessage }: UseEventSourceOptions` → `any`

**Exported Types:**
- `type EventSourceStatus`
- `type EventSourceEvent`
- `type UseEventSourceOptions`: url: string, withCredentials?: boolean, onMessage: (event: MessageEvent) => void

**Key Imports:** `react`

---

### apps\web-evals\src\hooks\use-open-router-models.ts
**Purpose:** Fetches and provides a list of available OpenRouter models.

**Exported Functions:**
- `getOpenRouterModels(): Promise<OpenRouterModel[]>` → `Promise<OpenRouterModel[]>`
- `useOpenRouterModels()` → `any`

**Exported Types:**
- `type OpenRouterModel`

**Key Imports:** `z`, `@tanstack/react-query`

---

### apps\web-evals\src\hooks\use-run-status.ts
**Purpose:** Provides real-time status updates for a given evaluation run.

**Exported Functions:**
- `useRunStatusrun: Run` → `RunStatus`

**Exported Types:**
- `type RunStatus`: sseStatus: EventSourceStatus, heartbeat: string | null | undefined, runners: string[] | undefined, tasks: (Task & { taskMetrics: TaskMetrics | null })[] | undefined, tokenUsage: Map<number, TokenUsage & { duration?: number }>, usageUpdatedAt: number | undefined

**Key Imports:** `react`, `@tanstack/react-query`, `@roo-code/types`, `@roo-code/evals`, `@/actions/heartbeat`

---

### apps\web-evals\src\lib\actions.ts
**Purpose:** Defines a server action to copy a run to production.

**Exported Functions:**
- `copyRunToProductionrunId: number` → `any`

**Key Imports:** `@roo-code/evals`

---

### apps\web-evals\src\lib\formatters.ts
**Purpose:** Provides utility functions for formatting data.

**Exported Functions:**
- `formatCurrencyamount: number` → `string`
- `formatDurationdurationMs: number` → `string`
- `formatTokenstokens: number` → `string`
- `formatToolUsageSuccessRateusage: { attempts: number; failures: number }` → `string`

---

### apps\web-evals\src\lib\schemas.ts
**Purpose:** Defines schemas for validating run creation data.

**Exported Types:**
- `type CreateRun`

**Exported Constants:**
- `MODEL_DEFAULT` = `"anthropic/claude-sonnet-4"`
- `CONCURRENCY_MIN` = `1`
- `CONCURRENCY_MAX` = `25`
- `CONCURRENCY_DEFAULT` = `1`
- `TIMEOUT_MIN` = `5`
- `TIMEOUT_MAX` = `10`
- `TIMEOUT_DEFAULT` = `5`

**Key Imports:** `z`, `@roo-code/types`

---

### apps\web-evals\src\lib\server\__tests__\sse-stream.spec.ts
---

### apps\web-evals\src\lib\server\redis.ts
**Purpose:** Provides a function to connect to a Redis instance.

**Exported Functions:**
- `redisClient()` → `Promise<RedisClientType>`

**Key Imports:** `redis`

---

### apps\web-evals\src\lib\server\sse-stream.ts
**Purpose:** Creates a server-sent events stream for real-time data updates.

**Exported Functions:**
- `constructor` → ``
- `writedata: string | object` → `Promise<boolean>`
- `close` → `Promise<void>`
- `getResponse` → `Response`

**Exported Types:**
- `class SSEStream`: _stream: TransformStream, _writer: WritableStreamDefaultWriter, _encoder: TextEncoder, _isClosed: boolean, isClosed: boolean

**Key Imports:** `TextEncoder`, `TransformStream`, `WritableStreamDefaultWriter`

---

### apps\web-evals\src\lib\utils.ts
**Purpose:** Provides utility functions, including a class name merger.

**Exported Functions:**
- `cn...inputs: ClassValue[]` → `string`

**Key Imports:** `clsx`, `tailwind-merge`

---

### apps\web-evals\vitest.config.ts
---

### apps\web-roo-code\next.config.ts
**Purpose:** Configures Next.js with redirects and extension aliases.

**Exported Functions:**
- `redirects` → `Promise<Redirect[]> | Redirect[]`

**Key Imports:** `next`

---

### apps\web-roo-code\src\actions\evals.ts
**Purpose:** Fetches and processes evaluation runs for display.

**Exported Functions:**
- `getEvalRuns` → `Promise<any>`

**Key Imports:** `@roo-code/types`, `@roo-code/evals`, `@/lib`

---

### apps\web-roo-code\src\app\enterprise\page.tsx
**Purpose:** Renders the Enterprise Solution page with metadata and content.

**Exported Types:**
- `type Metadata`: title, description, alternates, openGraph, twitter, keywords

**Exported Constants:**
- `TITLE` = `"Enterprise Solution"`
- `DESCRIPTION` = `"The control-plane for AI-powered software development. Gain visibility, governance, and control over your AI coding initiatives."`
- `PATH` = `"/enterprise"`

**Key Imports:** `lucide-react`, `@/components/ui`, `@/components/animated-text`, `@/lib/constants`, `next`, `@/lib/seo`

---

### apps\web-roo-code\src\app\evals\evals.tsx
**Purpose:** Displays evaluation runs in a table format with model information.

**Exported Functions:**
- `Evals{ runs: EvalRun[] }` → `JSX.Element`

**Key Imports:** `react`, `@/lib`, `@/lib/hooks`, `@/components/ui`, `./types`

---

### apps\web-roo-code\src\app\evals\page.tsx
**Purpose:** Fetches and renders evaluation runs on the evals page.

**Exported Constants:**
- `revalidate` = `300`
- `dynamic` = `"force-dynamic"`
- `TITLE` = `"Evals"`
- `DESCRIPTION` = `"Explore quantitative evals of LLM coding skills across tasks and providers."`
- `PATH` = `"/evals"`

**Key Imports:** `next`, `@/actions/evals`, `@/lib/seo`, `./evals`

---

### apps\web-roo-code\src\app\evals\plot.tsx
**Purpose:** Renders a scatter plot visualizing evaluation data.

**Exported Functions:**
- `Plot{ tableData }: PlotProps` → `JSX.Element`

**Exported Types:**
- `type PlotProps`: tableData: (EvalRun & { label: string; cost: number })[]

**Key Imports:** `react`, `recharts`, `@/lib`, `@/components/ui`, `./types`

---

### apps\web-roo-code\src\app\evals\types.ts
**Purpose:** Defines the EvalRun type for evaluation data.

**Exported Types:**
- `type EvalRun`: label: string, score: number, languageScores?: Record<"go" | "java" | "javascript" | "python" | "rust", number>, taskMetrics: TaskMetrics, modelId?: string

**Key Imports:** `@roo-code/evals`

---

### apps\web-roo-code\src\app\layout.tsx
**Purpose:** Defines the root layout with metadata, providers, and shell components.

**Exported Types:**
- `type Metadata`: metadataBase, title, description, alternates, icons, openGraph, twitter

**Exported Constants:**
- `inter` = `Inter`

**Key Imports:** `react`, `next`, `next/font/google`, `@/lib/seo`, `@/components/CookieConsentWrapper`, `@/components/providers`, `./globals.css`

---

### apps\web-roo-code\src\app\legal\cookies\page.tsx
**Purpose:** Renders the Cookie Policy page with relevant metadata.

**Exported Types:**
- `type Metadata`: title, description, alternates, openGraph, twitter, keywords

**Exported Constants:**
- `TITLE` = `"Cookie Policy"`
- `DESCRIPTION` = `"Learn about how Roo Code uses cookies to enhance your experience and provide our services."`
- `PATH` = `"/legal/cookies"`

**Key Imports:** `next`, `@/lib/seo`

---

### apps\web-roo-code\src\app\legal\subprocessors\page.tsx
**Purpose:** Displays a list of subprocessors used by Roo Code.

**Exported Types:**
- `type Metadata`: title, description, alternates, openGraph, twitter, keywords

**Exported Constants:**
- `TITLE` = `"Subprocessors"`
- `DESCRIPTION` = `"List of third-party subprocessors used by Roo Code to process customer data."`
- `PATH` = `"/legal/subprocessors"`

**Key Imports:** `next`, `@/lib/seo`

---

### apps\web-roo-code\src\app\page.tsx
**Purpose:** Renders the homepage with various interactive components.

**Exported Functions:**
- `Home` → `JSX.Element`

**Exported Constants:**
- `revalidate` = `3600`

**Key Imports:** `@/lib/stats`, `@/components/ui`, `@/components/homepage`, `@/lib/constants`, `lucide-react`, `@/components/structured-data`

---

### apps\web-roo-code\src\app\pricing\page.tsx
**Purpose:** Displays the pricing page with different plan options.

**Exported Types:**
- `interface PricingTier`: name: string, icon: LucideIcon, price: string, period?: string

**Exported Constants:**
- `TITLE` = `"Pricing - Roo Code Cloud"`
- `DESCRIPTION` = `"Simple, transparent pricing for Roo Code Cloud. The VS Code extension is free forever. Choose the cloud plan that fits your needs."`
- `PATH` = `"/pricing"`

**Key Imports:** `lucide-react`, `next`, `next/link`, `@/components/ui`, `@/components/homepage`, `@/lib/seo`, `@/lib/constants`

---

### apps\web-roo-code\src\app\privacy\page.tsx
**Purpose:** Renders the Privacy Policy page with relevant metadata.

**Exported Types:**
- `type Metadata`: title, description, alternates, openGraph, twitter, keywords

**Exported Constants:**
- `TITLE` = `"Privacy Policy"`
- `DESCRIPTION` = `"Privacy policy for Roo Code Cloud and marketing website. Learn how we handle your data and protect your privacy."`
- `PATH` = `"/privacy"`

**Key Imports:** `next`, `@/lib/seo`

---

### apps\web-roo-code\src\app\robots.ts
**Purpose:** Generates the robots.txt file for SEO and crawling.

**Exported Functions:**
- `robots` → `MetadataRoute.Robots`

**Key Imports:** `next`, `@/lib/seo`

---

### apps\web-roo-code\src\app\shell.tsx
**Purpose:** Provides a shell layout with navigation and footer components.

**Exported Functions:**
- `Shell{ children }: { children: React.ReactNode }` → `JSX.Element`

**Exported Constants:**
- `revalidate` = `3600`

**Key Imports:** `@/lib/stats`, `@/components/chromes`

---

### apps\web-roo-code\src\app\terms\page.tsx
**Purpose:** Renders the Terms of Service page with relevant metadata.

**Exported Types:**
- `type Metadata`: title, description, alternates, openGraph, twitter, keywords

**Exported Constants:**
- `TITLE` = `"Terms of Service"`
- `DESCRIPTION` = `"Terms of Service for Roo Code Cloud. Learn about our service terms, commercial conditions, and legal framework."`
- `PATH` = `"/terms"`

**Key Imports:** `next`, `@/lib/seo`

---

### apps\web-roo-code\src\components\animated-text.tsx
**Purpose:** Renders animated text using Framer Motion for visual effects.

**Exported Functions:**
- `AnimatedText({
		children, className
	}: AnimatedTextProps)` → `React.ReactNode`

**Exported Types:**
- `interface AnimatedTextProps`: children: React.ReactNode, className?: string

**Key Imports:** `react`, `framer-motion`

---

### apps\web-roo-code\src\components\chromes\footer.tsx
**Purpose:** Creates a responsive footer with links and theme toggling.

**Exported Functions:**
- `Footer()` → `React.ReactNode`

**Key Imports:** `react`, `next/link`, `next/image`, `lucide-react`, `next-themes`

---

### apps\web-roo-code\src\components\chromes\index.ts
**Purpose:** Exports all chrome components for easy importing.

---

### apps\web-roo-code\src\components\chromes\nav-bar.tsx
**Purpose:** Renders a navigation bar with logo, links, and theme toggle.

**Exported Functions:**
- `NavBar({ stars, downloads }: NavBarProps)` → `React.ReactNode`

**Exported Types:**
- `interface NavBarProps`: stars: string | null, downloads: string | null

**Key Imports:** `next/link`, `next/image`, `react`, `react-icons/rx`, `react-icons/vsc`, `lucide-react`, `next/navigation`

---

### apps\web-roo-code\src\components\chromes\stats-display.tsx
**Purpose:** Displays GitHub stars and VS Code downloads using links.

**Exported Functions:**
- `StatsDisplay()` → `JSX.Element`

**Key Imports:** `next/link`, `react-icons/rx`, `react-icons/vsc`, `@/lib/stats`

---

### apps\web-roo-code\src\components\chromes\theme-toggle.tsx
**Purpose:** Provides a theme toggle button for light and dark modes.

**Exported Functions:**
- `ThemeToggle()` → `JSX.Element`

**Key Imports:** `react`, `next-themes`, `react-icons/rx`, `@/components/ui`

---

### apps\web-roo-code\src\components\CookieConsentWrapper.tsx
**Purpose:** Manages and displays a GDPR-compliant cookie consent banner.

**Exported Functions:**
- `CookieConsentWrapper()` → `JSX.Element`

**Key Imports:** `react`, `react-cookie-consent`, `lucide-react`, `tldts`, `@roo-code/types`, `@/lib/analytics/consent-manager`

---

### apps\web-roo-code\src\components\enterprise\contact-form.tsx
**Purpose:** Renders a contact form with validation using Zod.

**Exported Functions:**
- `ContactForm({ formType, buttonText, buttonClassName }: ContactFormProps)` → `JSX.Element`

**Exported Types:**
- `interface ContactFormProps`: formType: "early-access" | "demo", buttonText: string, buttonClassName?: string

**Key Imports:** `react`, `zod`, `@/components/ui`

---

### apps\web-roo-code\src\components\homepage\animated-background.tsx
**Purpose:** Creates an animated background using a canvas element.

**Exported Functions:**
- `AnimatedBackground()` → `JSX.Element`

**Key Imports:** `react`

---

### apps\web-roo-code\src\components\homepage\code-example.tsx
**Purpose:** Displays a code example with a typing animation effect.

**Exported Functions:**
- `CodeExample()` → `JSX.Element`

**Key Imports:** `react`, `framer-motion`

---

### apps\web-roo-code\src\components\homepage\company-logos.tsx
**Purpose:** Renders a section displaying company logos with animation.

**Exported Functions:**
- `CompanyLogos()` → `JSX.Element`

**Key Imports:** `framer-motion`, `next/image`

---

### apps\web-roo-code\src\components\homepage\faq-section.tsx
**Purpose:** Displays a FAQ section with animated question/answer toggles.

**Exported Functions:**
- `FAQSection()` → `JSX.Element`

**Exported Types:**
- `interface FAQItem`: question: string, answer: React.ReactNode

**Key Imports:** `react`, `framer-motion`, `lucide-react`, `@/lib/utils`, `next/link`

---

### apps\web-roo-code\src\components\homepage\features.tsx
**Purpose:** Defines and renders a features section with icons and descriptions.

**Exported Types:**
- `interface Feature`: icon: LucideIcon, title: string, description: string, logos?: string[]

**Exported Constants:**
- `features` = `Feature[]`

**Key Imports:** `lucide-react`, `next/image`

---

### apps\web-roo-code\src\components\homepage\index.ts
**Purpose:** Exports all homepage components for easy importing.

---

### apps\web-roo-code\src\components\homepage\install-section.tsx
**Purpose:** Displays an install section with a VS Code download link.

**Exported Functions:**
- `InstallSection({ downloads }: InstallSectionProps)` → `JSX.Element`

**Exported Types:**
- `interface InstallSectionProps`: downloads: string | null

**Key Imports:** `react-icons/vsc`, `next/link`, `framer-motion`

---

### apps\web-roo-code\src\components\homepage\testimonials.tsx
**Purpose:** Renders a testimonial carousel with user reviews and ratings.

**Exported Types:**
- `interface Testimonial`: name: string, role: string, origin: string, quote: string, image?: string, stars?: number

**Exported Constants:**
- `testimonials` = `Testimonial[]`

**Key Imports:** `react`, `framer-motion`, `embla-carousel-react`, `embla-carousel-autoplay`, `lucide-react`

---

### apps\web-roo-code\src\components\homepage\whats-new-button.tsx
**Purpose:** Displays a button linking to a 'What's New' section.

**Exported Functions:**
- `WhatsNewButton()` → `JSX.Element`

**Exported Types:**
- `interface FeatureProps`: icon: React.ComponentType<{ className?: string }>, color: "blue" | "purple" | "green", title: string, description: string

**Key Imports:** `react`, `framer-motion`, `lucide-react`, `next/link`

---

### apps\web-roo-code\src\components\providers\google-analytics-provider.tsx
**Purpose:** Loads Google Tag Manager after user consent is given.

**Exported Functions:**
- `GoogleAnalyticsProvider{ children }: { children: React.ReactNode }` → `any`
- `initializeGoogleAnalytics` → `any`

**Exported Constants:**
- `GTM_ID` = `"AW-17391954825"`

**Key Imports:** `react`, `next/script`, `next-themes`, `@/lib/analytics/consent-manager`, `@/components/providers/posthog-provider`

---

### apps\web-roo-code\src\components\providers\index.ts
**Purpose:** Re-exports the providers component.

**Key Imports:** `./providers`

---

### apps\web-roo-code\src\components\providers\posthog-provider.tsx
**Purpose:** Provides PostHog analytics, tracking page views and user consent.

**Exported Functions:**
- `PageViewTracker` → `any`
- `PostHogProvider{ children }: { children: React.ReactNode }` → `any`
- `initializePosthog` → `any`

**Key Imports:** `next/navigation`, `posthog-js`, `react`, `@/lib/analytics/consent-manager`

---

### apps\web-roo-code\src\components\providers\providers.tsx
**Purpose:** Wraps application with providers for analytics and theming.

**Exported Functions:**
- `Providers{ children }: { children: React.ReactNode }` → `any`

**Key Imports:** `@tanstack/react-query`, `next-themes`, `./posthog-provider`, `./google-analytics-provider`

---

### apps\web-roo-code\src\components\structured-data.tsx
**Purpose:** Renders JSON-LD structured data for SEO in the document head.

**Exported Functions:**
- `StructuredData` → `any`

**Key Imports:** `@/lib/structured-data`

---

### apps\web-roo-code\src\components\ui\button.tsx
**Purpose:** Creates a reusable button component with various styling options.

**Exported Types:**
- `interface ButtonProps`: asChild?: boolean

**Key Imports:** `react`, `@radix-ui/react-slot`, `class-variance-authority`, `@/lib/utils`

---

### apps\web-roo-code\src\components\ui\chart.tsx
**Purpose:** Provides a chart component with theming and configuration options.

**Exported Types:**
- `type ChartConfig`: label?: React.ReactNode, icon?: React.ComponentType, color?: string, theme: Record<keyof typeof THEMES, string>

**Key Imports:** `react`, `recharts`, `@/lib/utils`

---

### apps\web-roo-code\src\components\ui\index.ts
**Purpose:** Exports UI components for button, chart, modal, scroll, and table.

**Key Imports:** `./button`, `./chart`, `./modal`, `./scroll-button`, `./table`

---

### apps\web-roo-code\src\components\ui\modal.tsx
**Purpose:** Creates modal components using Radix UI primitives.

**Exported Functions:**
- `DialogHeader` → `any`
- `DialogFooter` → `any`

**Key Imports:** `react`, `@radix-ui/react-dialog`, `lucide-react`, `@/lib/utils`

---

### apps\web-roo-code\src\components\ui\scroll-button.tsx
**Purpose:** Provides a button that scrolls to a target section on click.

**Exported Functions:**
- `ScrollButtonScrollButtonProps` → `any`

**Exported Types:**
- `interface ScrollButtonProps`: targetId: string, children: React.ReactNode, className?: string, onClick?: () => void

**Key Imports:** `next/navigation`, `react`

---

### apps\web-roo-code\src\components\ui\table.tsx
**Purpose:** Creates table components with header, body, and footer elements.

**Exported Types:**
- `interface TableProps`

**Key Imports:** `react`, `@/lib/utils`

---

### apps\web-roo-code\src\lib\analytics\consent-manager.ts
**Purpose:** Manages user consent for analytics using events and cookies.

**Exported Functions:**
- `hasConsent` → `boolean`
- `dispatchConsentEventconsented: boolean` → `void`
- `onConsentChangecallback: (consented: boolean) => void` → `() => void`

**Exported Constants:**
- `CONSENT_EVENT` = `"cookieConsentChanged"`

**Key Imports:** `react-cookie-consent`, `@roo-code/types`

---

### apps\web-roo-code\src\lib\constants.ts
**Purpose:** Defines external links used throughout the application.

**Exported Constants:**
- `EXTERNAL_LINKS` = `string`

---

### apps\web-roo-code\src\lib\format-currency.ts
**Purpose:** Formats currency amounts and parses price strings.

**Exported Functions:**
- `formatCurrencyamount: number | null | undefined` → `any`
- `parsePriceprice?: string` → `any`

---

### apps\web-roo-code\src\lib\format-duration.ts
**Purpose:** Formats a duration in milliseconds into a human-readable string.

**Exported Functions:**
- `formatDurationdurationMs: number | null | undefined` → `any`

---

### apps\web-roo-code\src\lib\format-score.ts
**Purpose:** Formats a score to a rounded percentage.

**Exported Functions:**
- `formatScorescore: number` → `any`

---

### apps\web-roo-code\src\lib\format-tokens.ts
**Purpose:** Formats token amounts with abbreviations (K, M, B).

**Exported Functions:**
- `formatTokenstokens: number | null | undefined, decimals = 0` → `any`

---

### apps\web-roo-code\src\lib\hooks\index.ts
**Purpose:** Exports custom hooks for the application.

**Key Imports:** `./use-logo-src`, `./use-open-router-models`

---

### apps\web-roo-code\src\lib\hooks\use-logo-src.ts
**Purpose:** Provides the correct logo source based on the current theme.

**Exported Functions:**
- `useLogoSrc` → `string`

**Key Imports:** `next-themes`, `react`

---

### apps\web-roo-code\src\lib\hooks\use-open-router-models.ts
**Purpose:** Fetches and provides OpenRouter model data using React Query.

**Exported Functions:**
- `parsePriceprice?: string` → `any`
- `useOpenRouterModels` → `any`

**Exported Types:**
- `type OpenRouterModel`
- `type OpenRouterModelRecord`

**Key Imports:** `zod`, `@tanstack/react-query`, `@roo-code/types`

---

### apps\web-roo-code\src\lib\index.ts
**Purpose:** Re-exports formatting utilities for currency, duration, and scores.

---

### apps\web-roo-code\src\lib\seo.ts
**Purpose:** Defines SEO configuration and related types for the application.

**Exported Types:**
- `type SeoConfig`

**Exported Constants:**
- `SITE_URL` = `https://roocode.com`
- `SEO` = `{ url: "https://roocode.com", name: "Roo Code", title: "Roo Code – The AI dev team that gets things done", description: "Roo Code puts an entire AI dev team right in your editor, outpacing closed tools with deep project-wide context, multi-step agentic coding, and unmatched developer-centric flexibility.", locale: "en_US", ogImage: { url: "/opengraph.png", width: 1200, height: 600, alt: "Roo Code" }, keywords: ["Roo Code", "AI coding agent", "VS Code extension", "AI pair programmer", "software development", "agentic coding", "code refactoring", "debugging"], category: "technology", twitterCard: "summary_large_image" }`

---

### apps\web-roo-code\src\lib\stats.ts
**Purpose:** Fetches and formats GitHub stars and VS Code extension reviews.

**Exported Functions:**
- `getGitHubStars` → `Promise<string | null>`
- `getVSCodeReviews` → `Promise<any[]>`

---

### apps\web-roo-code\src\lib\structured-data.ts
**Purpose:** Generates JSON-LD structured data for SEO purposes.

**Exported Functions:**
- `getStructuredData` → `StructuredDataGraph`

**Exported Types:**
- `interface ImageObject`: "@type", url, width, height
- `interface Organization`: "@type", "@id", name, url
- `interface WebSite`: "@type", "@id", url, name
- `interface SoftwareApplication`: "@type", "@id", name, applicationCategory
- `interface StructuredDataGraph`: "@context", "@graph"

**Key Imports:** `./seo`, `./constants`

---

### apps\web-roo-code\src\lib\utils.ts
**Purpose:** Provides utility functions, including a class name merger.

**Exported Functions:**
- `cn...inputs: ClassValue[]` → `string`

**Key Imports:** `clsx`, `tailwind-merge`

---

### apps\web-roo-code\tailwind.config.ts
**Purpose:** Configures the Tailwind CSS styles for the application.

**Key Imports:** `tailwindcss`

---

### packages\cloud\src\__mocks__\vscode.ts
---

### packages\cloud\src\__tests__\CloudService.integration.test.ts
---

### packages\cloud\src\__tests__\CloudService.test.ts
**Functions:** `expect`

---

### packages\cloud\src\__tests__\CloudSettingsService.parsing.test.ts
**Purpose:** Tests parsing of cloud settings responses from the CloudSettingsService.

**Key Imports:** `vscode`, `@roo-code/types`, `../CloudSettingsService.js`

---

### packages\cloud\src\__tests__\CloudSettingsService.test.ts
**Purpose:** Tests the CloudSettingsService, mocking dependencies and API calls.

**Key Imports:** `vscode`, `@roo-code/types`, `../CloudSettingsService.js`, `../RefreshTimer.js`

---

### packages\cloud\src\__tests__\CloudShareService.test.ts
**Purpose:** Tests the CloudShareService, focusing on sharing functionality.

**Key Imports:** `vitest`, `vscode`, `@roo-code/types`, `../CloudAPI.js`, `../CloudShareService.js`

---

### packages\cloud\src\__tests__\RefreshTimer.test.ts
**Purpose:** Tests the RefreshTimer, verifying immediate execution and backoff logic.

**Key Imports:** `vitest`, `../RefreshTimer.js`

---

### packages\cloud\src\__tests__\StaticSettingsService.test.ts
**Purpose:** Tests the StaticSettingsService, validating base64 and schema parsing.

**Key Imports:** `../StaticSettingsService.js`

---

### packages\cloud\src\__tests__\StaticTokenAuthService.spec.ts
**Purpose:** Tests the StaticTokenAuthService, validating token parsing and authentication.

**Key Imports:** `vscode`, `../StaticTokenAuthService.js`

---

### packages\cloud\src\__tests__\TelemetryClient.test.ts
**Purpose:** Tests the TelemetryClient, verifying event sending and data collection.

**Key Imports:** `@roo-code/types`, `../TelemetryClient.js`

---

### packages\cloud\src\__tests__\WebAuthService.spec.ts
**Purpose:** Tests the WebAuthService, focusing on authentication flow and token handling.

**Key Imports:** `crypto`, `vitest`, `vscode`, `../WebAuthService.js`, `../RefreshTimer.js`

---

### packages\cloud\src\bridge\__tests__\ExtensionChannel.test.ts
---

### packages\cloud\src\bridge\__tests__\TaskChannel.test.ts
---

### packages\cloud\src\bridge\BaseChannel.ts
**Purpose:** Defines an abstract base class for communication channels.

**Exported Functions:**
- `constructoroptions: BaseChannelOptions` → ``
- `onConnectsocket: Socket` → `Promise<void>`
- `onDisconnect` → `void`

**Exported Types:**
- `interface BaseChannelOptions`: instanceId, appProperties, gitProperties, isCloudAgent
- `class BaseChannel`: socket, instanceId, appProperties, gitProperties

**Key Imports:** `socket.io-client`, `vscode`, `@roo-code/types`

---

### packages\cloud\src\bridge\BridgeOrchestrator.ts
**Purpose:** Orchestrates communication between VS Code and the web application.

**Exported Functions:**
- `constructoroptions: BridgeOrchestratorOptions` → ``
- `connect` → `Promise<void>`
- `disconnect` → `Promise<void>`
- `handleConnectsocket: Socket` → `Promise<void>`
- `handleDisconnectreason: string` → `void`
- `handleReconnect` → `Promise<void>`

**Exported Types:**
- `interface BridgeOrchestratorOptions`: userId, socketBridgeUrl, token, provider, sessionId
- `class BridgeOrchestrator`: userId, socketBridgeUrl, token, provider, instanceId

**Key Imports:** `crypto`, `os`, `@roo-code/types`, `./SocketTransport.js`, `./ExtensionChannel.js`, `./TaskChannel.js`

---

### packages\cloud\src\bridge\ExtensionChannel.ts
**Purpose:** Manages the extension-level communication channel for the bridge.

**Exported Functions:**
- `constructoroptions: ExtensionChannelOptions` → ``
- `listenereventName: RooCodeEventName, listener: (...args: unknown[]) => void` → `void`

**Exported Types:**
- `interface ExtensionChannelOptions`: userId, provider
- `class ExtensionChannel`: userId, provider, extensionInstance, heartbeatInterval

**Key Imports:** `socket.io-client`, `@roo-code/types`, `./BaseChannel.js`

---

### packages\cloud\src\bridge\index.ts
**Purpose:** Exports bridge-related modules for cloud communication.

**Key Imports:** `./BridgeOrchestrator.js`, `./SocketTransport.js`, `./BaseChannel.js`, `./ExtensionChannel.js`, `./TaskChannel.js`

---

### packages\cloud\src\bridge\SocketTransport.ts
**Purpose:** Manages the WebSocket transport layer for the bridge system.

**Exported Functions:**
- `constructoroptions: SocketTransportOptions, retryConfig?: Partial<RetryConfig>` → ``

**Exported Types:**
- `interface SocketTransportOptions`: url, socketOptions, onConnect, onDisconnect, onReconnect
- `class SocketTransport`: socket, connectionState, retryTimeout, isPreviouslyConnected

**Key Imports:** `socket.io-client`, `@roo-code/types`

---

### packages\cloud\src\bridge\TaskChannel.ts
**Purpose:** Manages task-level communication channels within the bridge.

**Exported Functions:**
- `constructoroptions: TaskChannelOptions` → ``
- `listenereventName: TaskBridgeEventName, listener: TaskEventListener` → `void`

**Exported Types:**
- `interface TaskChannelOptions`
- `class TaskChannel`: subscribedTasks, pendingTasks, taskListeners, eventMapping

**Key Imports:** `socket.io-client`, `@roo-code/types`, `./BaseChannel.js`

---

### packages\cloud\src\CloudAPI.ts
**Purpose:** Provides an API client for interacting with the Roo Code cloud.

**Exported Types:**
- `class CloudAPI`: authService, log, baseUrl

**Key Imports:** `zod`, `@roo-code/types`, `./config.js`, `./utils.js`, `./errors.js`

---

### packages\cloud\src\CloudService.ts
**Purpose:** Manages the cloud service, handling authentication and settings.

**Exported Types:**
- `class CloudService`: context, authStateListener, authUserInfoListener, settingsList

**Key Imports:** `vscode`, `events`, `@roo-code/types`, `./errors.js`, `./WebAuthService.js`, `./StaticTokenAuthService.js`, `./CloudSettingsService.js`, `./StaticSettingsService.js`, `./TelemetryClient.js`, `./CloudShareService.js`, `./CloudAPI.js`, `./retry-queue/index.js`

---

### packages\cloud\src\CloudSettingsService.ts
**Purpose:** Provides settings management for the cloud service.

**Exported Types:**
- `class CloudSettingsService`

**Key Imports:** `events`, `vscode`, `zod`, `@roo-code/types`, `./config.js`, `./RefreshTimer.js`

---

### packages\cloud\src\CloudShareService.ts
**Purpose:** Shares tasks using the Cloud API and VS Code clipboard.

**Exported Functions:**
- `shareTasktaskId: string, visibility: ShareVisibility = "organization"` → `Promise<ShareResponse>`
- `canShareTask` → `Promise<boolean>`

**Exported Types:**
- `class CloudShareService`: cloudAPI: CloudAPI, settingsService: SettingsService, log: (...args: unknown[]) => void

**Key Imports:** `@roo-code/types`, `./importVscode.js`, `./CloudAPI.js`

---

### packages\cloud\src\config.ts
**Purpose:** Provides configuration variables for Clerk and RooCode API URLs.

**Exported Functions:**
- `getClerkBaseUrl` → ``
- `getRooCodeApiUrl` → ``

**Exported Constants:**
- `PRODUCTION_CLERK_BASE_URL` = `https://clerk.roocode.com`
- `PRODUCTION_ROO_CODE_API_URL` = `https://app.roocode.com`

---

### packages\cloud\src\errors.ts
**Purpose:** Defines custom error classes for Cloud API interactions.

**Exported Types:**
- `class CloudAPIError`: message: string, statusCode?: number, responseBody?: unknown
- `class TaskNotFoundError`: taskId?: string
- `class AuthenticationError`: message = "Authentication required"
- `class NetworkError`: message = "Network error occurred"
- `class InvalidClientTokenError`

---

### packages\cloud\src\importVscode.ts
**Purpose:** Dynamically imports the VS Code module if available.

**Exported Functions:**
- `importVscode` → `Promise<typeof import("vscode") | undefined>`

---

### packages\cloud\src\index.ts
**Purpose:** Exports cloud service modules and related types.

**Exported Types:**
- `interface QueuedRequest`: id: string, url: string, options: RequestInit, timestamp: number, retryCount: number
- `interface QueueStats`: totalQueued: number, byType: Record<string, number>, oldestRequest?: Date, newestRequest?: Date
- `interface RetryQueueConfig`: maxRetries: number, retryDelay: number, maxQueueSize: number
- `interface RetryQueueEvents`

**Key Imports:** `./config.js`, `./CloudService.js`, `./bridge/index.js`, `./retry-queue/index.js`

---

### packages\cloud\src\RefreshTimer.ts
**Purpose:** Provides a timer with configurable retry behavior for callbacks.

**Exported Types:**
- `interface RefreshTimerOptions`: callback: () => Promise<boolean>, successInterval?: number, initialBackoffMs?: number, maxBackoffMs?: number
- `class RefreshTimer`: callback: () => Promise<boolean>, successInterval: number, initialBackoffMs: number, maxBackoffMs: number

---

### packages\cloud\src\retry-queue\__tests__\RetryQueue.test.ts
---

### packages\cloud\src\retry-queue\index.ts
**Purpose:** Exports RetryQueue and related types for handling API retries.

**Exported Types:**
- `interface QueuedRequest`: id: string, url: string, options: RequestInit, timestamp: number, retryCount: number
- `interface QueueStats`: totalQueued: number, byType: Record<string, number>, oldestRequest?: Date, newestRequest?: Date
- `interface RetryQueueConfig`: maxRetries: number, retryDelay: number, maxQueueSize: number
- `interface RetryQueueEvents`

**Key Imports:** `./RetryQueue.js`, `./types.js`

---

### packages\cloud\src\retry-queue\RetryQueue.ts
**Purpose:** Manages a queue for retrying API requests with exponential backoff.

**Exported Types:**
- `class RetryQueue`: queue: Map<string, QueuedRequest>, context: ExtensionContext, config: RetryQueueConfig, log: (...args: unknown[]) => void

**Key Imports:** `events`, `vscode`, `./types.js`

---

### packages\cloud\src\retry-queue\types.ts
**Purpose:** Defines types for retry queue requests, stats, and configuration.

**Exported Types:**
- `interface QueuedRequest`: id: string, url: string, options: RequestInit, timestamp: number, retryCount: number
- `interface QueueStats`: totalQueued: number, byType: Record<string, number>, oldestRequest?: Date, newestRequest?: Date
- `interface RetryQueueConfig`: maxRetries: number, retryDelay: number, maxQueueSize: number
- `interface RetryQueueEvents`

---

### packages\cloud\src\StaticSettingsService.ts
**Purpose:** Provides static settings from a base64 encoded environment variable.

**Exported Types:**
- `class StaticSettingsService`: settings: OrganizationSettings, log: (...args: unknown[]) => void

**Key Imports:** `@roo-code/types`

---

### packages\cloud\src\StaticTokenAuthService.ts
**Purpose:** Implements AuthService using a static JWT token.

**Exported Types:**
- `class StaticTokenAuthService`: state: AuthState, token: string, log: (...args: unknown[]) => void, userInfo: CloudUserInfo

**Key Imports:** `events`, `jwt-decode`, `vscode`, `@roo-code/types`

---

### packages\cloud\src\TelemetryClient.ts
**Purpose:** Abstract class for telemetry clients with event filtering.

**Exported Types:**
- `class TelemetryClient`: subscription?: TelemetryEventSubscription, debug = false

**Key Imports:** `@roo-code/types`, `./config.js`, `./retry-queue/index.js`

---

### packages\cloud\src\utils.ts
**Purpose:** Provides utility functions, like generating a user agent string.

**Exported Functions:**
- `getUserAgentcontext?: ExtensionContext` → `string`

**Key Imports:** `vscode`

---

### packages\cloud\src\WebAuthService.ts
**Purpose:** Implements AuthService using web-based authentication flows.

**Exported Types:**
- `type AuthCredentials`

**Key Imports:** `crypto`, `events`, `vscode`, `zod`, `@roo-code/types`, `./config.js`

---

### packages\cloud\vitest.config.ts
**Purpose:** Configures Vitest for cloud package testing with aliases.

**Key Imports:** `vitest/config`

---

### packages\config-eslint\base.js
**Purpose:** Provides a shared ESLint configuration for the repository.

**Exported Constants:**
- `config` = `string`

**Key Imports:** `@eslint/js`, `eslint-config-prettier`, `eslint-plugin-turbo`, `typescript-eslint`, `eslint-plugin-only-warn`

---

### packages\config-eslint\next.js
**Purpose:** Extends React ESLint config for Next.js projects.

**Exported Constants:**
- `nextJsConfig` = `string`

**Key Imports:** `@next/eslint-plugin-next`, `./react.js`

---

### packages\config-eslint\react.js
**Purpose:** Defines a React-specific ESLint configuration.

**Exported Constants:**
- `reactConfig` = `string`

**Key Imports:** `@eslint/js`, `eslint-config-prettier`, `typescript-eslint`, `eslint-plugin-react-hooks`, `eslint-plugin-react`, `globals`, `./base.js`

---

### packages\evals\drizzle.config.ts
**Purpose:** Configures Drizzle for database migrations.

**Exported Constants:**
- `default` = `string`

**Key Imports:** `drizzle-kit`

---

### packages\evals\src\cli\index.ts
**Purpose:** Provides the command-line interface for running evals.

**Exported Functions:**
- `main()` → `Promise<void>`

**Key Imports:** `fs`, `cmd-ts`, `../exercises/index.js`, `./runCi.js`, `./runEvals.js`, `./runTask.js`

---

### packages\evals\src\cli\redis.ts
**Purpose:** Manages Redis connections and provides utility functions.

**Exported Functions:**
- `redisClient()` → `Promise<RedisClientType | undefined>`
- `getPubSubKey(runId: number)` → `string`
- `getRunnersKey(runId: number)` → `string`
- `getHeartbeatKey(runId: number)` → `string`
- `registerRunner({ runId, taskId, timeoutSeconds }: { runId: number; taskId: number; timeoutSeconds: number })` → `Promise<void>`
- `deregisterRunner({ runId, taskId }: { runId: number; taskId: number })` → `Promise<void>`
- `startHeartbeat(runId: number, seconds: number = 10)` → `Promise<NodeJS.Timer>`
- `stopHeartbeat(interval: NodeJS.Timer)` → `void`

**Key Imports:** `redis`

---

### packages\evals\src\cli\runCi.ts
**Purpose:** Runs evals in CI mode, creating tasks for each exercise.

**Exported Functions:**
- `runCi({ concurrency, exercisesPerLanguage }: { concurrency?: number; exercisesPerLanguage?: number } = {})` → `Promise<void>`

**Key Imports:** `p-map`, `../exercises/index.js`, `../db/index.js`, `./runEvals.js`

---

### packages\evals\src\cli\runEvals.ts
**Purpose:** Orchestrates the execution of eval tasks based on run ID.

**Exported Functions:**
- `runEvals(runId: number)` → `Promise<void>`

**Key Imports:** `p-queue`, `../db/index.js`, `../exercises/index.js`, `./utils.js`, `./redis.js`, `./runTask.js`

---

### packages\evals\src\cli\runTask.ts
**Purpose:** Processes individual eval tasks, handling execution and logging.

**Exported Functions:**
- `processTask({ taskId, logger }: { taskId: number; logger?: Logger })` → `Promise<void>`
- `publish(runId: number, event: TaskEvent)` → `Promise<void>`
- `processTaskInContainer({ taskId, logger }: { taskId: number; logger?: Logger })` → `Promise<void>`
- `runTask(task: Task, logger?: Logger)` → `Promise<void>`

**Exported Types:**
- `class SubprocessTimeoutError`: constructor(timeout: number), name, message

**Key Imports:** `fs`, `path`, `os`, `pWaitFor`, `execa`, `@roo-code/types`, `@roo-code/ipc`, `../db/index.js`, `../exercises/index.js`, `./utils.js`, `./redis.js`, `./runUnitTest.js`

---

### packages\evals\src\cli\runUnitTest.ts
**Purpose:** Runs unit tests for a given task using specified commands.

**Exported Functions:**
- `runUnitTest({ task, logger }: RunUnitTestOptions)` → `Promise<void>`

**Exported Types:**
- `type RunUnitTestOptions`: task: Task, logger: Logger

**Key Imports:** `path`, `execa`, `psTree`, `../db/index.js`, `../exercises/index.js`

---

### packages\evals\src\cli\utils.ts
**Purpose:** Provides utility functions for CLI operations and logging.

**Exported Functions:**
- `getTag(caller: string, { run, task }: { run: Run; task?: Task })` → `string`
- `isDockerContainer()` → `() => boolean`
- `resetEvalsRepo({ run, cwd }: { run: Run; cwd: string })` → `Promise<void>`
- `commitEvalsRepoChanges({ run, cwd }: { run: Run; cwd: string })` → `Promise<void>`

**Exported Types:**
- `interface LoggerOptions`: logDir: string, filename: string, tag: string
- `class Logger`: logStream: fs.WriteStream | undefined, logFilePath: string, tag: string
- `enum LogLevel`: INFO, ERROR, WARN, DEBUG

**Key Imports:** `fs`, `path`, `execa`, `../db/index.js`

---

### packages\evals\src\db\db.ts
**Purpose:** Manages database connections and provides client instances.

**Exported Functions:**
- `getProductionClient()` → `() => any`
- `disconnect()` → `Promise<void>`

**Exported Types:**
- `type DatabaseOrTransaction`: typeof client, Parameters<Parameters<typeof client.transaction>[0]>[0]

**Key Imports:** `drizzle-orm/postgres-js`, `postgres`, `./schema.js`

---

### packages\evals\src\db\index.ts
**Purpose:** Exports database schema, queries, and database connection.

**Key Imports:** `./schema.js`, `./queries/runs.js`, `./queries/tasks.js`, `./queries/taskMetrics.js`, `./queries/toolErrors.js`

---

### packages\evals\src\db\queries\__tests__\copyRun.spec.ts
---

### packages\evals\src\db\queries\__tests__\runs.test.ts
---

### packages\evals\src\db\queries\copyRun.ts
**Purpose:** Copies a run and its associated data to a target database.

**Exported Functions:**
- `copyRun({ sourceDb, targetDb, runId }: { sourceDb: NodePgDatabase<typeof schema>; targetDb: NodePgDatabase<typeof schema>; runId: number })` → `Promise<void>`

**Key Imports:** `drizzle-orm`, `drizzle-orm/node-postgres`, `../schema.js`, `./errors.js`

---

### packages\evals\src\db\queries\errors.ts
**Purpose:** Defines custom error classes for database operations.

**Exported Types:**
- `class RecordNotFoundError`
- `class RecordNotCreatedError`

---

### packages\evals\src\db\queries\runs.ts
**Purpose:** Provides functions for managing and querying run data.

**Exported Functions:**
- `findRun(id: number)` → `Promise<any>`
- `createRun(args: InsertRun)` → `Promise<any>`
- `updateRun(id: number, values: UpdateRun)` → `Promise<any>`
- `getRuns()` → `Promise<any>`
- `finishRun(runId: number)` → `Promise<any>`
- `deleteRun(id: number)` → `Promise<void>`

**Key Imports:** `drizzle-orm`, `@roo-code/types`, `./errors.js`, `../schema.js`, `../db.js`, `./taskMetrics.js`, `./tasks.js`

---

### packages\evals\src\db\queries\taskMetrics.ts
**Purpose:** Manages task metrics data within the database.

**Exported Functions:**
- `findTaskMetrics(id: number)` → `Promise<any>`
- `createTaskMetrics(args: InsertTaskMetrics)` → `Promise<any>`
- `updateTaskMetrics(id: number, values: UpdateTaskMetrics)` → `Promise<any>`

**Key Imports:** `drizzle-orm`, `./errors.js`, `../schema.js`, `../db.js`

---

### packages\evals\src\db\queries\tasks.ts
**Purpose:** Provides functions for managing and querying task data.

**Exported Functions:**
- `findTask(id: number)` → `Promise<any>`
- `createTask(args: InsertTask)` → `Promise<any>`
- `updateTask(id: number, values: UpdateTask)` → `Promise<any>`
- `getTask({ runId, language, exercise }: GetTask)` → `Promise<any>`
- `getTasks(runId: number)` → `Promise<any>`
- `getLanguageScores(runId: number)` → `Promise<any>`

**Key Imports:** `drizzle-orm`, `../../exercises/index.js`, `./errors.js`, `../schema.js`, `../db.js`

---

### packages\evals\src\db\queries\toolErrors.ts
**Purpose:** Creates tool error records in the database.

**Exported Functions:**
- `createToolError(args: InsertToolError)` → `Promise<any>`

**Key Imports:** `./errors.js`, `../schema.js`, `../db.js`

---

### packages\evals\src\db\schema.ts
**Purpose:** Defines database schema using Drizzle ORM.

**Exported Types:**
- `type Run`: id: integer, taskMetricsId: integer, model: text, name: text
- `type InsertRun`: model: text, name: text, description: text, contextWindow: integer
- `type UpdateRun`: model?: text, name?: text, description?: text, contextWindow?: integer
- `type Task`: id: integer, runId: integer, taskMetricsId: integer, language: ExerciseLanguage
- `type InsertTask`: runId: number, language: ExerciseLanguage, exercise: string, model: string
- `type UpdateTask`: runId?: number, taskMetricsId?: number, language?: ExerciseLanguage, exercise?: string
- `type TaskMetrics`: id: integer, tokensIn: number, tokensOut: number, tokensContext: number
- `type InsertTaskMetrics`: tokensIn: number, tokensOut: number, tokensContext: number, cacheWrites: number
- `type UpdateTaskMetrics`: tokensIn?: number, tokensOut?: number, tokensContext?: number, cacheWrites?: number
- `type ToolError`: id: integer, taskId: number, toolName: ToolName, message: string
- `type InsertToolError`: taskId: number, toolName: ToolName, message: string, stack?: string

**Key Imports:** `drizzle-orm/pg-core`, `drizzle-orm`, `@roo-code/types`, `../exercises/index.js`

---

### packages\evals\src\exercises\index.ts
**Purpose:** Provides functions for listing and retrieving exercise directories.

**Exported Functions:**
- `listDirectories(basePath: string, relativePath: string)` → `Promise<string[]>`
- `getExercisesForLanguage(basePath: string, language: ExerciseLanguage)` → `Promise<string[]>`

**Exported Types:**
- `type ExerciseLanguage`

**Exported Constants:**
- `EVALS_REPO_PATH` = `string`
- `exerciseLanguages` = `readonly ["go", "java", "javascript", "python", "rust"]`

**Key Imports:** `path`, `fs/promises`, `url`

---

### packages\evals\src\index.ts
**Purpose:** Exports database and exercise related modules.

**Key Imports:** `./db/index.js`, `./exercises/index.js`

---

### packages\evals\vitest-global-setup.ts
**Functions:** `resetTestDatabase`, `function`

---

### packages\evals\vitest.config.ts
---

### packages\ipc\src\index.ts
---

### packages\ipc\src\ipc-client.ts
**Purpose:** Implements an IPC client for communication with a server.

**Exported Types:**
- `class IpcClient`: _socketPath: string, _id: string, _log: (...args: unknown[]) => void, _isConnected: boolean

**Key Imports:** `node:events`, `node:crypto`, `node-ipc`, `@roo-code/types`

---

### packages\ipc\src\ipc-server.ts
**Purpose:** Implements an IPC server for inter-process communication.

**Exported Types:**
- `class IpcServer`: _socketPath: string, _log: (...args: unknown[]) => void, _clients: Map<string, Socket>, _isListening: boolean

**Key Imports:** `node:events`, `node:net`, `node:crypto`, `node-ipc`, `@roo-code/types`

---

### packages\telemetry\src\__tests__\PostHogTelemetryClient.test.ts
---

### packages\telemetry\src\BaseTelemetryClient.ts
**Purpose:** Defines an abstract base class for telemetry clients and event handling.

**Exported Functions:**
- `constructorsubscription?: TelemetryEventSubscription, protected readonly debug = false` → ``

**Exported Types:**
- `class BaseTelemetryClient`: subscription?: TelemetryEventSubscription, debug: boolean, providerRef: WeakRef<TelemetryPropertiesProvider> | null, telemetryEnabled: boolean

**Key Imports:** `@roo-code/types`, `TelemetryEvent`, `TelemetryEventName`, `TelemetryClient`, `TelemetryPropertiesProvider`

---

### packages\telemetry\src\index.ts
**Purpose:** Exports all modules within the telemetry package for external use.

**Key Imports:** `./BaseTelemetryClient`, `./PostHogTelemetryClient`, `./TelemetryService`

---

### packages\telemetry\src\PostHogTelemetryClient.ts
**Purpose:** Implements a telemetry client using PostHog for event tracking.

**Exported Functions:**
- `constructordebug = false` → ``
- `captureevent: TelemetryEvent` → `Promise<void>`

**Exported Types:**
- `class PostHogTelemetryClient`: client: PostHog, distinctId: string, gitPropertyNames: string[]

**Key Imports:** `posthog-node`, `vscode`, `@roo-code/types`, `TelemetryEventName`, `BaseTelemetryClient`

---

### packages\telemetry\src\TelemetryService.ts
**Purpose:** Provides a service to manage and dispatch telemetry events to clients.

**Exported Functions:**
- `constructorprivate clients: TelemetryClient[]` → ``
- `registerclient: TelemetryClient` → `void`
- `setProviderprovider: TelemetryPropertiesProvider` → `void`
- `updateTelemetryStateisOptedIn: boolean` → `void`

**Exported Types:**
- `class TelemetryService`: clients: TelemetryClient[]

**Key Imports:** `ZodError`, `@roo-code/types`, `TelemetryClient`, `TelemetryPropertiesProvider`, `TelemetryEventName`

---

### packages\telemetry\vitest.config.ts
---

### packages\types\src\__tests__\cloud.test.ts
---

### packages\types\src\__tests__\index.test.ts
---

### packages\types\src\__tests__\ipc.test.ts
---

### packages\types\src\__tests__\provider-settings.test.ts
---

### packages\types\src\api.ts
**Purpose:** Defines the RooCode API interface for interacting with the extension.

**Exported Types:**
- `interface RooCodeAPI`: startNewTask, resumeTask, isTaskInHistory, getCurrentTaskStack

**Key Imports:** `events`, `net`, `RooCodeEvents`, `RooCodeSettings`, `ProviderSettingsEntry`

---

### packages\types\src\cloud.ts
**Purpose:** Defines cloud-related interfaces and data structures for Roo Code.

**Exported Types:**
- `interface JWTPayload`: iss?: string, sub?: string, exp?: number, iat?: number
- `interface CloudUserInfo`: id?: string, name?: string, email?: string, picture?: string
- `interface CloudOrganization`: id: string, name: string, slug?: string

**Key Imports:** `events`, `zod`, `RooCodeEventName`, `TaskStatus`, `globalSettingsSchema`

---

### packages\types\src\codebase-index.ts
**Purpose:** Defines configuration and models for codebase indexing features.

**Exported Types:**
- `type CodebaseIndexConfig`: codebaseIndexEnabled, codebaseIndexQdrantUrl, codebaseIndexEmbedderProvider, codebaseIndexEmbedderBaseUrl

**Exported Constants:**
- `CODEBASE_INDEX_DEFAULTS` = `{"MIN_SEARCH_RESULTS":10,"MAX_SEARCH_RESULTS":200,"DEFAULT_SEARCH_RESULTS":50,"SEARCH_RESULTS_STEP":10,"MIN_SEARCH_SCORE":0,"MAX_SEARCH_SCORE":1,"DEFAULT_SEARCH_MIN_SCORE":0.4,"SEARCH_SCORE_STEP":0.05}`

**Key Imports:** `zod`

---

### packages\types\src\cookie-consent.ts
**Purpose:** Provides types and constants related to cookie consent management.

**Exported Types:**
- `type ConsentCookieValue`

**Exported Constants:**
- `CONSENT_COOKIE_NAME` = `"roo-code-cookie-consent"`
- `COOKIE_CONSENT_EVENTS` = `{"CHANGED":"cookieConsentChanged"}`

---

### packages\types\src\events.ts
**Purpose:** Defines event names and schemas for Roo Code's event system.

**Exported Types:**
- `enum RooCodeEventName`

**Key Imports:** `zod`, `clineMessageSchema`, `tokenUsageSchema`, `toolNamesSchema`

---

### packages\types\src\experiment.ts
**Purpose:** Defines experiment IDs, schemas, and types for feature flags.

**Exported Types:**
- `type ExperimentId`
- `type Experiments`

**Exported Constants:**
- `experimentIds` = `["powerSteering","multiFileApplyDiff","preventFocusDisruption","imageGeneration","runSlashCommand"]`

**Key Imports:** `zod`, `Keys`, `Equals`, `AssertEqual`

---

### packages\types\src\followup.ts
**Purpose:** Defines interfaces and schemas for follow-up questions in tasks.

**Exported Types:**
- `interface FollowUpData`: question?: string, suggest?: Array<SuggestionItem>
- `interface SuggestionItem`: answer: string, mode?: string
- `type FollowUpDataType`

**Key Imports:** `zod`

---

### packages\types\src\global-settings.ts
**Purpose:** Defines global settings and their schemas for Roo Code.

**Exported Types:**
- `type globalSettingsSchema`

**Exported Constants:**
- `DEFAULT_WRITE_DELAY_MS` = `1000`
- `DEFAULT_TERMINAL_OUTPUT_CHARACTER_LIMIT` = `50000`

**Key Imports:** `zod`, `Keys`, `ProviderSettings`, `PROVIDER_SETTINGS_KEYS`, `providerSettingsEntrySchema`

---

### packages\types\src\history.ts
**Purpose:** Defines the structure for storing task history items.

**Exported Types:**
- `type HistoryItem`

**Key Imports:** `zod`

---

### packages\types\src\index.ts
**Purpose:** Exports all types and modules within the types package.

**Key Imports:** `./api.js`, `./cloud.js`, `./codebase-index.js`, `./cookie-consent.js`, `./events.js`

---

### packages\types\src\ipc.ts
**Purpose:** Defines types and schemas for inter-process communication (IPC).

**Exported Types:**
- `enum IpcMessageType`
- `enum IpcOrigin`
- `type Ack`
- `enum TaskCommandName`
- `type TaskCommand`

**Key Imports:** `zod`, `TaskEvent`, `taskEventSchema`, `rooCodeSettingsSchema`

---

### packages\types\src\marketplace.ts
**Purpose:** Defines types and schemas for marketplace items and components.

**Exported Types:**
- `type McpParameter`
- `type McpInstallationMethod`
- `type MarketplaceItemType`

**Key Imports:** `zod`

---

### packages\types\src\mcp.ts
**Purpose:** Defines types and schemas related to MCP (Marketplace Component Protocol).

**Exported Types:**
- `interface McpServerUse`: type: string, serverName: string, toolName?: string, uri?: string
- `type McpExecutionStatus`

**Key Imports:** `zod`

---

### packages\types\src\message.ts
**Purpose:** Defines types and constants related to LLM interaction requests.

**Exported Constants:**
- `clineAsks` = `[...]`

**Key Imports:** `z`

---

### packages\types\src\mode.ts
**Purpose:** Defines schemas and types for configuring different operational modes.

**Exported Types:**
- `type GroupOptions`: fileRegex, description
- `type GroupEntry`

**Exported Constants:**
- `groupOptionsSchema`
- `groupEntrySchema`
- `modeConfigSchema`

**Key Imports:** `z`, `./tool.js`

---

### packages\types\src\model.ts
**Purpose:** Defines types and schemas related to model parameters and settings.

**Exported Types:**
- `type ReasoningEffort`
- `type ReasoningEffortWithMinimal`
- `type VerbosityLevel`
- `type ServiceTier`
- `type ModelParameter`

**Exported Constants:**
- `reasoningEfforts` = `[...]`
- `verbosityLevels` = `[...]`
- `serviceTiers` = `[...]`
- `modelParameters` = `[...]`

**Key Imports:** `z`

---

### packages\types\src\provider-settings.ts
**Purpose:** Defines settings and types for different AI providers and models.

**Exported Types:**
- `type DynamicProvider`
- `type LocalProvider`

**Exported Constants:**
- `DEFAULT_CONSECUTIVE_MISTAKE_LIMIT` = `3`
- `dynamicProviders` = `[...]`
- `localProviders` = `[...]`

**Key Imports:** `z`, `./model.js`, `./codebase-index.js`, `./providers/index.js`

---

### packages\types\src\providers\__tests__\claude-code.spec.ts
---

### packages\types\src\providers\anthropic.ts
**Purpose:** Provides model definitions and metadata for Anthropic models.

**Exported Types:**
- `type AnthropicModelId`

**Exported Constants:**
- `anthropicDefaultModelId` = `"claude-sonnet-4-20250514"`
- `anthropicModels`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\bedrock.ts
**Purpose:** Defines model IDs and metadata for Amazon Bedrock models.

**Exported Types:**
- `type BedrockModelId`

**Exported Constants:**
- `bedrockDefaultModelId` = `"anthropic.claude-sonnet-4-20250514-v1:0"`
- `bedrockDefaultPromptRouterModelId` = `"anthropic.claude-3-sonnet-20240229-v1:0"`
- `bedrockModels`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\cerebras.ts
**Purpose:** Provides model definitions and metadata for Cerebras models.

**Exported Types:**
- `type CerebrasModelId`

**Exported Constants:**
- `cerebrasDefaultModelId` = `"qwen-3-coder-480b-free"`
- `cerebrasModels`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\chutes.ts
**Purpose:** Defines model IDs for Chutes AI models.

**Exported Types:**
- `type ChutesModelId`

**Exported Constants:**
- `chutesDefaultModelId` = `"deepseek-ai/DeepSeek-V3-0324"`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\claude-code.ts
**Purpose:** Manages Claude Code model IDs and Vertex AI compatibility.

**Exported Functions:**
- `convertModelNameForVertexmodelName: string` → `string`

**Exported Types:**
- `type ClaudeCodeModelId`

**Key Imports:** `../model.js`, `./anthropic.js`

---

### packages\types\src\providers\deepinfra.ts
**Purpose:** Provides default values for DeepInfra model configurations.

**Exported Constants:**
- `deepInfraDefaultModelId` = `"Qwen/Qwen3-Coder-480B-A35B-Instruct-Turbo"`
- `deepInfraDefaultModelInfo`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\deepseek.ts
**Purpose:** Defines model IDs and metadata for DeepSeek models.

**Exported Types:**
- `type DeepSeekModelId`

**Exported Constants:**
- `deepSeekDefaultModelId` = `"deepseek-chat"`
- `deepSeekModels`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\doubao.ts
**Purpose:** Provides model definitions and metadata for Doubao models.

**Exported Constants:**
- `doubaoDefaultModelId` = `"doubao-seed-1-6-250615"`
- `doubaoModels`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\featherless.ts
**Purpose:** Defines model IDs and metadata for Featherless models.

**Exported Types:**
- `type FeatherlessModelId`

**Exported Constants:**
- `featherlessModels`
- `featherlessDefaultModelId`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\fireworks.ts
**Purpose:** Provides model definitions and metadata for Fireworks models.

**Exported Types:**
- `type FireworksModelId`

**Exported Constants:**
- `fireworksDefaultModelId` = `"accounts/fireworks/models/kimi-k2-instruct-0905"`
- `fireworksModels`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\gemini.ts
**Purpose:** Defines model IDs and metadata for Google Gemini models.

**Exported Types:**
- `type GeminiModelId`

**Exported Constants:**
- `geminiDefaultModelId` = `"gemini-2.0-flash-001"`
- `geminiModels`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\glama.ts
**Purpose:** Provides default model and configuration for Glama.

**Exported Constants:**
- `glamaDefaultModelId` = `"anthropic/claude-3-7-sonnet"`
- `glamaDefaultModelInfo`
- `GLAMA_DEFAULT_TEMPERATURE` = `0`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\groq.ts
**Purpose:** Defines Groq model IDs and related metadata for the provider.

**Exported Types:**
- `type GroqModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\huggingface.ts
**Purpose:** Declares constants for HuggingFace provider configuration and UI.

**Exported Constants:**
- `HUGGINGFACE_DEFAULT_MAX_TOKENS` = `2048`
- `HUGGINGFACE_MAX_TOKENS_FALLBACK` = `8192`
- `HUGGINGFACE_DEFAULT_CONTEXT_WINDOW` = `128_000`
- `HUGGINGFACE_SLIDER_STEP` = `256`
- `HUGGINGFACE_SLIDER_MIN` = `1`
- `HUGGINGFACE_TEMPERATURE_MAX_VALUE` = `2`
- `HUGGINGFACE_API_URL` = `"https://router.huggingface.co/v1/models?collection=roocode"`
- `HUGGINGFACE_CACHE_DURATION` = `1000 * 60 * 60`

---

### packages\types\src\providers\index.ts
**Purpose:** Exports all provider modules for easy access and use.

---

### packages\types\src\providers\io-intelligence.ts
**Purpose:** Defines IO Intelligence model IDs and related metadata.

**Exported Types:**
- `type IOIntelligenceModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\lite-llm.ts
**Purpose:** Provides LiteLLM default model ID and related model information.

**Exported Constants:**
- `litellmDefaultModelId` = `"claude-3-7-sonnet-20250219"`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\lm-studio.ts
**Purpose:** Defines LM Studio default model ID and related model information.

**Exported Constants:**
- `LMSTUDIO_DEFAULT_TEMPERATURE` = `0`
- `lMStudioDefaultModelId` = `"mistralai/devstral-small-2505"`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\mistral.ts
**Purpose:** Defines Mistral model IDs and related metadata for the provider.

**Exported Types:**
- `type MistralModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\moonshot.ts
**Purpose:** Defines Moonshot model IDs and related metadata for the provider.

**Exported Types:**
- `type MoonshotModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\ollama.ts
**Purpose:** Defines Ollama default model ID and related model information.

**Exported Constants:**
- `ollamaDefaultModelId` = `"devstral:24b"`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\openai.ts
**Purpose:** Defines OpenAI native model IDs and related metadata.

**Exported Types:**
- `type OpenAiNativeModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\openrouter.ts
**Purpose:** Defines OpenRouter default model ID and related model information.

**Exported Constants:**
- `OPENROUTER_DEFAULT_PROVIDER_NAME` = `"[default]"`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\qwen-code.ts
**Purpose:** Defines Qwen Code model IDs and related metadata.

**Exported Types:**
- `type QwenCodeModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\requesty.ts
**Purpose:** Defines Requesty default model ID and related model information.

**Exported Constants:**
- `requestyDefaultModelId` = `"coding/claude-4-sonnet"`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\roo.ts
**Purpose:** Defines Roo model IDs and related metadata for the provider.

**Exported Types:**
- `type RooModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\sambanova.ts
**Purpose:** Defines SambaNova model IDs and related metadata.

**Exported Types:**
- `type SambaNovaModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\unbound.ts
**Purpose:** Defines Unbound default model ID and related model information.

**Exported Constants:**
- `unboundDefaultModelId` = `"anthropic/claude-3-7-sonnet-20250219"`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\vercel-ai-gateway.ts
**Purpose:** Defines Vercel AI Gateway default model ID and related constants.

**Exported Constants:**
- `vercelAiGatewayDefaultModelId` = `"anthropic/claude-sonnet-4"`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\vertex.ts
**Purpose:** Defines Vertex model IDs and related metadata for the provider.

**Exported Types:**
- `type VertexModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\vscode-llm.ts
**Purpose:** Defines VSCode LLM model IDs and related metadata.

**Exported Types:**
- `type VscodeLlmModelId`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\xai.ts
**Purpose:** Defines types and constants for xAI model providers and configurations.

**Exported Types:**
- `type XAIModelId`

**Exported Constants:**
- `xaiDefaultModelId` = `"grok-code-fast-1"`
- `xaiModels` = `{...}`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\zai.ts
**Purpose:** Provides types and constants for Zhipu AI (Z AI) model configurations.

**Exported Types:**
- `type InternationalZAiModelId`

**Exported Constants:**
- `internationalZAiDefaultModelId` = `"glm-4.5"`
- `internationalZAiModels` = `{...}`

**Key Imports:** `type { ModelInfo } from "../model.js"`, `import { ZaiApiLine } from "../provider-settings.js"`

---

### packages\types\src\single-file-read-models.ts
**Purpose:** Determines if a model should use the single-file read format.

**Exported Functions:**
- `shouldUseSingleFileReadmodelId: string` → `boolean`

---

### packages\types\src\task.ts
**Purpose:** Defines interfaces and types related to task management and providers.

**Exported Types:**
- `interface TaskProviderLike`: getCurrentTask(): TaskLike | undefined, getRecentTasks(): string[], createTask(text?: string, images?: string[], parentTask?: TaskLike, options?: CreateTaskOptions, configuration?: RooCodeSettings,): Promise<TaskLike>, cancelTask(): Promise<void>, clearTask(): Promise<void>

**Key Imports:** `import { z } from "zod"`, `import type { RooCodeSettings } from "./global-settings.js"`, `import type { ClineMessage, QueuedMessage, TokenUsage } from "./message.js"`, `import type { ToolUsage, ToolName } from "./tool.js"`, `import type { StaticAppProperties, GitProperties, TelemetryProperties } from "./telemetry.js"`, `import type { TodoItem } from "./todo.js"`

---

### packages\types\src\telemetry.ts
**Purpose:** Defines telemetry settings, event names, and related schemas.

**Exported Types:**
- `type TelemetrySetting`
- `enum TelemetryEventName`

**Exported Constants:**
- `telemetrySettings` = `["unset", "enabled", "disabled"]`

**Key Imports:** `import { z } from "zod"`, `import { providerNames } from "./provider-settings.js"`, `import { clineMessageSchema } from "./message.js"`

---

### packages\types\src\terminal.ts
**Purpose:** Defines types for command execution status within a terminal.

**Exported Types:**
- `type CommandExecutionStatus`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\src\todo.ts
**Purpose:** Defines types and schemas for todo items and their statuses.

**Exported Types:**
- `type TodoStatus`
- `type TodoItem`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\src\tool.ts
**Purpose:** Defines types, schemas, and constants related to tools and their usage.

**Exported Types:**
- `type ToolGroup`
- `type ToolName`
- `type ToolUsage`

**Exported Constants:**
- `toolGroups` = `["read", "edit", "browser", "command", "mcp", "modes"]`
- `toolNames` = `["execute_command", "read_file", "write_to_file", "apply_diff", "insert_content", "search_and_replace", "search_files", "list_files", "list_code_definition_names", "browser_action", "use_mcp_tool", "access_mcp_resource", "ask_followup_question", "attempt_completion", "switch_mode", "new_task", "fetch_instructions", "codebase_search", "update_todo_list", "run_slash_command", "generate_image"]`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\src\type-fu.ts
**Purpose:** Provides utility types for type manipulation and assertions.

**Exported Types:**
- `type Keys`
- `type Values`
- `type Equals`
- `type AssertEqual`

---

### packages\types\src\vscode.ts
**Purpose:** Defines types and constants related to VS Code extensions.

**Exported Types:**
- `type CodeActionId`
- `type CodeActionName`
- `type TerminalActionId`
- `type TerminalActionName`
- `type TerminalActionPromptType`
- `type CommandId`
- `type Language`

**Exported Constants:**
- `codeActionIds` = `["explainCode", "fixCode", "improveCode", "addToContext", "newTask"]`
- `terminalActionIds` = `["terminalAddToContext", "terminalFixCommand", "terminalExplainCommand"]`
- `commandIds` = `["activationCompleted", "plusButtonClicked", "promptsButtonClicked", "mcpButtonClicked", "historyButtonClicked", "marketplaceButtonClicked", "popoutButtonClicked", "cloudButtonClicked", "settingsButtonClicked", "openInNewTab", "showHumanRelayDialog", "registerHumanRelayCallback", "unregisterHumanRelayCallback", "handleHumanRelayResponse", "newTask", "setCustomStoragePath", "importSettings", "focusInput", "acceptInput", "focusPanel", "toggleAutoApprove"]`
- `languages` = `["ca", "de", "en", "es", "fr", "hi", "id", "it", "ja", "ko", "nl", "pl", "pt-BR", "ru", "tr", "vi"]`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\tsup.config.ts
---

### packages\types\vitest.config.ts
---

### scripts\find-missing-i18n-key.js
**Purpose:** Finds missing i18n keys in component files across locales.

**Key Imports:** `const fs = require("fs")`, `const path = require("path")`

---

### scripts\find-missing-translations.js
**Purpose:** Identifies missing translations in locale files based on English.

**Key Imports:** `const path = require("path")`, `const { promises: fs } = require("fs")`

---

### scripts\install-vsix.js
**Purpose:** Installs a VSIX package for the Roo Code extension.

**Key Imports:** `const { execSync } = require("child_process")`, `const fs = require("fs")`, `const readline = require("readline")`

---

### scripts\update-contributors.js
**Purpose:** Fetches contributor data from GitHub and updates the README.md file.

**Exported Functions:**
- `parseLinkHeaderheader: string` → `any`
- `httpGeturl: string, options: any` → `Promise<any>`
- `fetchContributorsPageurl: string` → `Promise<any>`
- `fetchContributorsoptions: any` → `Promise<any>`
- `readReadmepath: string` → `Promise<string>`
- `formatContributorsSectioncontributors: any` → `string`
- `updateReadmereadmeContent: string, contributorsSection: string` → `Promise<void>`
- `writeReadmepath: string, content: string` → `Promise<void>`
- `findLocalizedReadmeslocalesDir: string` → `Promise<string[]>`
- `updateLocalizedReadmereadmePath: string, contributorsSection: string` → `Promise<void>`
- `main` → `Promise<void>`
- `createCellcontributor: any` → `string`

**Exported Constants:**
- `GITHUB_API_URL` = `"https://api.github.com/repos/RooCodeInc/Roo-Code/contributors?per_page=100"`
- `README_PATH` = `path.join(__dirname, "..", "README.md")`
- `LOCALES_DIR` = `path.join(__dirname, "..", "locales")`
- `START_MARKER` = `"<!-- START CONTRIBUTORS SECTION - AUTO-GENERATED, DO NOT EDIT MANUALLY -->"`
- `END_MARKER` = `"<!-- END CONTRIBUTORS SECTION -->"`

**Key Imports:** `https`, `fs`, `util`, `path`

---

### src\__mocks__\fs\promises.ts
**Functions:** `ensureDirectoryExists`

---

### src\__mocks__\vscode.js
**Functions:** `mockEventEmitter`, `constructor`

---

### src\__tests__\command-integration.spec.ts
---

### src\__tests__\command-mentions.spec.ts
**Functions:** `callParseMentions`

---

### src\__tests__\commands.spec.ts
---

### src\__tests__\dist_assets.spec.ts
---

### src\__tests__\extension.spec.ts
**Functions:** `instance`

---

### src\__tests__\migrateSettings.spec.ts
---

### src\activate\__tests__\CodeActionProvider.spec.ts
---

### src\activate\__tests__\registerCommands.spec.ts
---

### src\activate\CodeActionProvider.ts
**Purpose:** Provides code actions for explaining, fixing, and improving code with Roo Code.

**Exported Types:**
- `class CodeActionProvider`: providedCodeActionKinds, createAction, provideCodeActions

**Exported Constants:**
- `TITLES` = `{
	EXPLAIN: "Explain with Roo Code",
	FIX: "Fix with Roo Code",
	IMPROVE: "Improve with Roo Code",
	ADD_TO_CONTEXT: "Add to Roo Code",
	NEW_TASK: "New Roo Code Task",
} as const`

**Key Imports:** `vscode`, `@roo-code/types`, `../shared/package`, `../utils/commands`, `../integrations/editor/EditorUtils`

---

### src\activate\handleTask.ts
**Purpose:** Handles the creation of new tasks within the Roo Code extension.

**Exported Functions:**
- `handleNewTaskparams: { prompt?: string } | null | undefined` → `Promise<void>`

**Key Imports:** `vscode`, `../shared/package`, `../core/webview/ClineProvider`, `../i18n`

---

### src\activate\handleUri.ts
**Purpose:** Handles URIs to manage callbacks from various cloud services.

**Exported Functions:**
- `handleUriuri: vscode.Uri` → `Promise<void>`

**Key Imports:** `vscode`, `@roo-code/cloud`, `../core/webview/ClineProvider`

---

### src\activate\humanRelay.ts
**Purpose:** Manages callbacks for human relay responses within the extension.

**Exported Functions:**
- `registerHumanRelayCallbackrequestId: string, callback: (response: string | undefined) => void` → `void`
- `unregisterHumanRelayCallbackrequestId: string` → `void`
- `handleHumanRelayResponseresponse: { requestId: string; text?: string; cancelled?: boolean }` → `void`

---

### src\activate\index.ts
**Purpose:** Exports modules for handling URIs, commands, and code actions.

**Key Imports:** `./handleUri`, `./registerCommands`, `./registerCodeActions`, `./registerTerminalActions`, `./CodeActionProvider`

---

### src\activate\registerCodeActions.ts
**Purpose:** Registers code actions for the Roo Code extension in VS Code.

**Exported Functions:**
- `registerCodeActionscontext: vscode.ExtensionContext` → `void`
- `registerCodeActioncontext: vscode.ExtensionContext, command: CodeActionId, promptType: CodeActionName` → `void`

**Key Imports:** `vscode`, `@roo-code/types`, `../utils/commands`, `../integrations/editor/EditorUtils`, `../core/webview/ClineProvider`

---

### src\activate\registerCommands.ts
**Purpose:** Registers commands for the Roo Code extension in VS Code.

**Exported Functions:**
- `getVisibleProviderOrLogoutputChannel: vscode.OutputChannel` → `ClineProvider | undefined`
- `getPanel` → `vscode.WebviewPanel | vscode.WebviewView | undefined`
- `setPanelpanel: vscode.WebviewPanel | vscode.WebviewView | undefined, mode: "sidebar" | "tab"` → `void`
- `registerCommandscontext: vscode.ExtensionContext` → `void`
- `openClineInNewTab` → `Promise<void>`

**Key Imports:** `vscode`, `delay`, `@roo-code/types`, `@roo-code/telemetry`, `../shared/package`, `../utils/commands`, `../core/webview/ClineProvider`, `../core/config/ContextProxy`, `../utils/focusPanel`, `./humanRelay`, `./handleTask`, `../services/code-index/manager`, `../core/config/importExport`, `../services/mdm/MdmService`, `../i18n`

---

### src\activate\registerTerminalActions.ts
**Purpose:** Registers terminal actions for the Roo Code extension in VS Code.

**Exported Functions:**
- `registerTerminalActionscontext: vscode.ExtensionContext` → `void`
- `registerTerminalActioncontext: vscode.ExtensionContext, command: TerminalActionId, promptType: TerminalActionPromptType` → `void`

**Key Imports:** `vscode`, `@roo-code/types`, `../utils/commands`, `../core/webview/ClineProvider`, `../integrations/terminal/Terminal`, `../i18n`

---

### src\api\index.ts
**Purpose:** Defines API handlers for various AI providers and message metadata.

**Exported Types:**
- `interface SingleCompletionHandler`: completePrompt
- `interface ApiHandlerCreateMessageMetadata`: mode, taskId, previousResponseId, suppressPreviousResponseId

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `./transform/stream`, `./providers`

---

### src\api\providers\__tests__\anthropic-vertex.spec.ts
**Functions:** `await`

---

### src\api\providers\__tests__\anthropic.spec.ts
**Functions:** `await`

---

### src\api\providers\__tests__\bedrock-custom-arn.spec.ts
**Purpose:** Tests Bedrock handler's custom ARN functionality using mocks.

**Key Imports:** `../bedrock`, `../../../shared/api`, `../../../utils/logging`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\providers\__tests__\bedrock-error-handling.spec.ts
**Purpose:** Tests error handling capabilities of the AwsBedrockHandler.

**Key Imports:** `../bedrock`, `@anthropic-ai/sdk`, `@aws-sdk/credential-providers`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\providers\__tests__\bedrock-inference-profiles.spec.ts
**Purpose:** Tests Amazon Bedrock inference profile mappings and handler creation.

**Exported Constants:**
- `AWS_INFERENCE_PROFILE_MAPPING` = `string`

**Key Imports:** `@roo-code/types`, `../bedrock`, `../../../shared/api`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\providers\__tests__\bedrock-invokedModelId.spec.ts
**Purpose:** Tests the AwsBedrockHandler's invoked model ID functionality.

**Key Imports:** `../../../shared/api`, `../bedrock`, `@aws-sdk/credential-providers`, `@smithy/smithy-client`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\providers\__tests__\bedrock-reasoning.spec.ts
**Purpose:** Tests extended thinking support within the AwsBedrockHandler.

**Key Imports:** `../bedrock`, `@aws-sdk/client-bedrock-runtime`, `../../../utils/logging`

---

### src\api\providers\__tests__\bedrock-vpc-endpoint.spec.ts
**Purpose:** Tests Amazon Bedrock VPC endpoint configuration and validation.

**Key Imports:** `../bedrock`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\providers\__tests__\bedrock.spec.ts
**Purpose:** Tests the AwsBedrockHandler class and its methods.

**Key Imports:** `../bedrock`, `@aws-sdk/client-bedrock-runtime`, `@roo-code/types`, `@anthropic-ai/sdk`

---

### src\api\providers\__tests__\cerebras.spec.ts
**Purpose:** Tests the CerebrasHandler class and its methods.

**Key Imports:** `../cerebras`, `@roo-code/types`

---

### src\api\providers\__tests__\chutes.spec.ts
**Purpose:** Tests the ChutesHandler class and its interaction with OpenAI.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../chutes`

---

### src\api\providers\__tests__\claude-code-caching.spec.ts
**Purpose:** Tests ClaudeCodeHandler's caching support and token collection.

**Key Imports:** `@anthropic-ai/sdk`, `../claude-code`, `../../../integrations/claude-code/run`, `../../transform/stream`

---

### src\api\providers\__tests__\claude-code.spec.ts
**Purpose:** Tests the ClaudeCodeHandler and its model configuration.

**Key Imports:** `../claude-code`, `../../../shared/api`, `../../../integrations/claude-code/types`, `../../../integrations/claude-code/run`, `../../../integrations/claude-code/message-filter`

---

### src\api\providers\__tests__\constants.spec.ts
**Purpose:** Tests the DEFAULT_HEADERS constant for correct values.

**Exported Constants:**
- `DEFAULT_HEADERS` = `string`

**Key Imports:** `../constants`, `../../../shared/package`

---

### src\api\providers\__tests__\deepseek.spec.ts
**Purpose:** Tests the DeepseekHandler class and its methods.

**Key Imports:** `openai`, `@roo-code/types`

---

### src\api\providers\__tests__\featherless.spec.ts
**Purpose:** Tests the FeatherlessHandler and its OpenAI integration.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../featherless`

---

### src\api\providers\__tests__\fireworks.spec.ts
**Purpose:** Tests the FireworksHandler and its OpenAI integration.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../fireworks`

---

### src\api\providers\__tests__\gemini-handler.spec.ts
**Functions:** `mockReturnValue`

---

### src\api\providers\__tests__\gemini.spec.ts
**Purpose:** Tests GeminiHandler class, verifying constructor and message creation.

**Exported Functions:**
- `createMessageAnthropic.Messages.MessageParam[]` → `any`

**Exported Types:**
- `class GeminiHandler`: options: any, client: any, getModel(): ModelInfo, createMessage(messages: any): any, completePrompt(prompt: string): any

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `i18next`, `../gemini`

---

### src\api\providers\__tests__\glama.spec.ts
**Purpose:** Tests GlamaHandler, mocking dependencies and OpenAI client.

**Key Imports:** `@anthropic-ai/sdk`, `../glama`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\groq.spec.ts
**Purpose:** Tests GroqHandler, verifying API key and model selection.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../groq`

---

### src\api\providers\__tests__\io-intelligence.spec.ts
**Purpose:** Tests IOIntelligenceHandler, mocking OpenAI and fetcher functions.

**Key Imports:** `@anthropic-ai/sdk`, `../io-intelligence`, `../../../shared/api`

---

### src\api\providers\__tests__\lite-llm.spec.ts
**Purpose:** Tests LiteLLMHandler, mocking OpenAI and model fetching.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `../lite-llm`, `../../../shared/api`, `@roo-code/types`

---

### src\api\providers\__tests__\lm-studio-timeout.spec.ts
**Purpose:** Tests LmStudioHandler timeout configuration using mocked utilities.

**Key Imports:** `../lm-studio`, `../../../shared/api`, `../utils/timeout-config`, `openai`

---

### src\api\providers\__tests__\lmstudio.spec.ts
**Purpose:** Tests LmStudioHandler, mocking OpenAI and verifying responses.

**Key Imports:** `../lm-studio`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\mistral.spec.ts
**Purpose:** Tests MistralHandler, mocking Mistral client and verifying responses.

**Key Imports:** `@anthropic-ai/sdk`, `../mistral`, `../../../shared/api`, `../../transform/stream`, `@mistralai/mistralai`

---

### src\api\providers\__tests__\moonshot.spec.ts
**Purpose:** Tests MoonshotHandler, mocking OpenAI and verifying usage metrics.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`

---

### src\api\providers\__tests__\native-ollama.spec.ts
**Purpose:** Tests NativeOllamaHandler, mocking Ollama and verifying message streaming.

**Key Imports:** `../native-ollama`, `../../../shared/api`, `ollama`

---

### src\api\providers\__tests__\ollama-timeout.spec.ts
**Purpose:** Tests OllamaHandler timeout configuration using mocked utilities.

**Key Imports:** `../ollama`, `../../../shared/api`, `../utils/timeout-config`, `openai`

---

### src\api\providers\__tests__\ollama.spec.ts
**Purpose:** Tests OllamaHandler, mocking OpenAI and verifying responses.

**Key Imports:** `@anthropic-ai/sdk`, `../ollama`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\openai-native-usage.spec.ts
**Purpose:** Tests OpenAiNativeHandler, normalizing usage metrics from responses.

**Key Imports:** `vitest`, `../openai-native`, `@roo-code/types`

---

### src\api\providers\__tests__\openai-native.spec.ts
**Purpose:** Tests OpenAiNativeHandler, mocking OpenAI and verifying responses.

**Key Imports:** `@anthropic-ai/sdk`, `../openai-native`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\openai-timeout.spec.ts
**Purpose:** Tests OpenAI handler timeout configuration using mocks and expectations.

**Key Imports:** `../openai`, `../../../shared/api`, `../utils/timeout-config`, `openai`

---

### src\api\providers\__tests__\openai-usage-tracking.spec.ts
**Purpose:** Tests OpenAI handler's usage tracking with mocked completion streams.

**Key Imports:** `@anthropic-ai/sdk`, `../../../shared/api`, `../openai`, `openai`

---

### src\api\providers\__tests__\openai.spec.ts
**Purpose:** Tests OpenAI handler functionality, including streaming and usage metrics.

**Key Imports:** `../openai`, `../../../shared/api`, `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../../shared/package`, `axios`

---

### src\api\providers\__tests__\openrouter.spec.ts
**Purpose:** Tests OpenRouterHandler, mocking dependencies for model and API interactions.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `../openrouter`, `../../../shared/api`, `../../../shared/package`

---

### src\api\providers\__tests__\requesty.spec.ts
**Purpose:** Tests RequestyHandler, verifying initialization and API interactions.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `../requesty`, `../../../shared/api`, `../../../shared/package`

---

### src\api\providers\__tests__\roo.spec.ts
**Purpose:** Tests Roo handler, mocking OpenAI and verifying completion responses.

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\sambanova.spec.ts
**Purpose:** Tests SambaNovaHandler, verifying base URL and API key usage.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../sambanova`

---

### src\api\providers\__tests__\unbound.spec.ts
**Purpose:** Tests UnboundHandler, mocking model cache and verifying behavior.

**Key Imports:** `@anthropic-ai/sdk`, `../../../shared/api`, `../unbound`

---

### src\api\providers\__tests__\vercel-ai-gateway.spec.ts
**Purpose:** Tests VercelAiGatewayHandler, mocking dependencies and verifying functionality.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `../vercel-ai-gateway`, `../../../shared/api`, `@roo-code/types`

---

### src\api\providers\__tests__\vertex.spec.ts
**Purpose:** Tests VertexHandler, mocking client and verifying streaming responses.

**Key Imports:** `@anthropic-ai/sdk`, `../../transform/stream`, `i18next`, `../vertex`

---

### src\api\providers\__tests__\vscode-lm.spec.ts
**Purpose:** Tests VsCodeLmHandler, mocking vscode and verifying chat functionality.

**Key Imports:** `vscode`, `../vscode-lm`, `../../../shared`

---

### src\api\providers\__tests__\xai.spec.ts
**Purpose:** Tests XAIHandler, verifying base URL and API key usage.

**Key Imports:** `openai`, `type`, `@roo-code/types`, `../xai`

---

### src\api\providers\__tests__\zai.spec.ts
**Purpose:** Tests ZAiHandler, verifying base URLs and API key usage.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../zai`

---

### src\api\providers\anthropic-vertex.ts
**Purpose:** Provides an Anthropic Vertex AI API handler for completions.

**Exported Types:**
- `class AnthropicVertexHandler`: options, client, constructor, completePrompt

**Key Imports:** `@anthropic-ai/sdk`, `@anthropic-ai/vertex-sdk`, `google-auth-library`, `@roo-code/types`, `../../shared/api`, `../../shared/safeJsonParse`, `../transform/stream`, `../transform/caching/vertex`, `../transform/model-params`, `./base-provider`

---

### src\api\providers\anthropic.ts
**Purpose:** Implements an Anthropic API handler for AI model interactions.

**Exported Types:**
- `class AnthropicHandler`: options, client, constructor, completePrompt

**Key Imports:** `@anthropic-ai/sdk`, `@anthropic-ai/sdk/streaming`, `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/model-params`, `./base-provider`, `../../shared/cost`

---

### src\api\providers\base-openai-compatible-provider.ts
**Purpose:** Provides a base class for OpenAI-compatible API providers.

**Exported Types:**
- `class BaseOpenAiCompatibleProvider`: providerName, baseURL, defaultTemperature, defaultProviderModelId, providerModels, options, client, constructor, getModel

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/openai-format`, `./constants`, `./base-provider`, `./utils/openai-error-handler`

---

### src\api\providers\base-provider.ts
**Purpose:** Defines a base class for API providers with common functionalities.

**Exported Types:**
- `class BaseProvider`: createMessage, getModel, countTokens

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../transform/stream`, `../../utils/countTokens`

---

### src\api\providers\bedrock.ts
**Purpose:** Implements a Bedrock API handler for interacting with AWS Bedrock models.

**Exported Types:**
- `class AnthropicVertexHandler`: options, client, constructor, completePrompt

**Key Imports:** `@aws-sdk/client-bedrock-runtime`, `@aws-sdk/credential-providers`, `@anthropic-ai/sdk`, `@roo-code/types`, `../transform/stream`, `./base-provider`, `../../utils/logging`, `../transform/cache-strategy/multi-point-strategy`, `../transform/cache-strategy/types`, `../transform/bedrock-converse-format`, `../transform/model-params`, `../../shared/api`

---

### src\api\providers\cerebras.ts
**Purpose:** Provides Cerebras API interaction, handling message formatting and token stripping.

**Exported Functions:**
- `stripThinkingTokenstext: string` → `string`
- `flattenMessageContentcontent: any` → `string`
- `convertToCerebrasMessagesmessages: any` → `any`
- `constructoroptions: ApiHandlerOptions` → `any`

**Exported Constants:**
- `CEREBRAS_BASE_URL` = `https://api.cerebras.ai/v1`
- `CEREBRAS_DEFAULT_TEMPERATURE` = `0`

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../../shared/api`, `../../shared/cost`, `../transform/stream`

---

### src\api\providers\chutes.ts
**Purpose:** Manages Chutes API interactions, extending OpenAI compatibility for completions.

**Exported Functions:**
- `constructoroptions: ApiHandlerOptions` → `any`
- `getModel` → `any`

**Exported Types:**
- `class ChutesHandler`: providerName, baseURL, apiKey, defaultProviderModelId, providerModels

**Key Imports:** `@roo-code/types`, `@anthropic-ai/sdk`, `openai`, `../../shared/api`, `../transform/r1-format`

---

### src\api\providers\claude-code.ts
**Purpose:** Handles Claude Code API interactions, filtering messages and running code.

**Exported Functions:**
- `constructoroptions: ApiHandlerOptions` → `any`
- `getModel` → `any`

**Exported Types:**
- `class ClaudeCodeHandler`: options, createMessage, getModel

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../transform/stream`, `../../integrations/claude-code/run`, `../../i18n`

---

### src\api\providers\constants.ts
**Purpose:** Defines default HTTP headers for API requests.

**Exported Constants:**
- `DEFAULT_HEADERS` = `{...}`

**Key Imports:** `../../shared/package`

---

### src\api\providers\deepinfra.ts
**Purpose:** Provides DeepInfra API integration, extending RouterProvider for model handling.

**Exported Functions:**
- `constructoroptions: ApiHandlerOptions` → `any`
- `getModel` → `any`

**Exported Types:**
- `class DeepInfraHandler`: options, name, baseURL, apiKey, modelId

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\deepseek.ts
**Purpose:** Manages DeepSeek API interactions, extending OpenAI handler with specific logic.

**Exported Functions:**
- `constructoroptions: ApiHandlerOptions` → `any`
- `getModel` → `any`

**Exported Types:**
- `class DeepSeekHandler`: options, getModel, processUsageMetrics

**Key Imports:** `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/model-params`, `./openai`

---

### src\api\providers\doubao.ts
**Purpose:** Provides Doubao API integration, extending OpenAI handler for completions.

**Exported Functions:**
- `constructoroptions: ApiHandlerOptions` → `any`
- `getModel` → `any`

**Exported Types:**
- `interface ChatCompletionMessageParam`: role, content
- `interface ChatCompletionParams`: model, messages, temperature, stream
- `class DoubaoHandler`: openAiApiKey, openAiModelId, openAiBaseUrl, openAiStreamingEnabled, includeMaxTokens

**Key Imports:** `./openai`, `../../shared/api`, `@roo-code/types`, `../transform/model-params`, `../transform/stream`

---

### src\api\providers\fake-ai.ts
**Purpose:** Defines a FakeAI provider for testing and mocking API interactions.

**Exported Types:**
- `interface FakeAI`: id, removeFromCache, createMessage, getModel
- `class FakeAIHandle`: id, removeFromCache, createMessage, getModel

**Key Imports:** `@anthropic-ai/sdk`, `../index`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\featherless.ts
**Purpose:** Manages Featherless API interactions, extending OpenAI compatibility for completions.

**Exported Functions:**
- `constructoroptions: ApiHandlerOptions` → `any`
- `getModel` → `any`

**Exported Types:**
- `class FeatherlessHandler`: providerName, baseURL, apiKey, defaultProviderModelId, providerModels

**Key Imports:** `@roo-code/types`, `@anthropic-ai/sdk`, `openai`, `../../shared/api`, `../transform/r1-format`

---

### src\api\providers\fetchers\__tests__\litellm.spec.ts
---

### src\api\providers\fetchers\__tests__\lmstudio.test.ts
---

### src\api\providers\fetchers\__tests__\modelCache.spec.ts
---

### src\api\providers\fetchers\__tests__\ollama.test.ts
---

### src\api\providers\fetchers\__tests__\openrouter.spec.ts
---

### src\api\providers\fetchers\__tests__\vercel-ai-gateway.spec.ts
---

### src\api\providers\fetchers\deepinfra.ts
**Purpose:** Fetches and parses DeepInfra model information from the API.

**Exported Functions:**
- `getDeepInfraModelsapiKey?: string, baseUrl: string = "https://api.deepinfra.com/v1/openai"` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../constants`

---

### src\api\providers\fetchers\glama.ts
**Purpose:** Retrieves and processes model information from the Glama API.

**Exported Functions:**
- `getGlamaModels` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `../../../shared/cost`

---

### src\api\providers\fetchers\huggingface.ts
**Purpose:** Fetches and parses Hugging Face model data from the API.

**Exported Types:**
- `type HuggingFaceProvider`: provider, status, supports_tools, supports_structured_output

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../../../shared/api`

---

### src\api\providers\fetchers\io-intelligence.ts
**Purpose:** Fetches and parses IO Intelligence model data from the API.

**Exported Types:**
- `type IOIntelligenceModel`: id, object, created, owned_by, root

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../../../shared/api`

---

### src\api\providers\fetchers\litellm.ts
**Purpose:** Fetches model information from a LiteLLM server.

**Exported Functions:**
- `getLiteLLMModelsapiKey: string, baseUrl: string` → `Promise<ModelRecord>`

**Key Imports:** `axios`, `@roo-code/types`, `../../../shared/api`, `../constants`

---

### src\api\providers\fetchers\lmstudio.ts
**Purpose:** Fetches and parses LM Studio model details and manages cache.

**Exported Functions:**
- `hasLoadedFullDetailsmodelId: string` → `boolean`
- `forceFullModelDetailsLoadbaseUrl: string, modelId: string` → `Promise<void>`
- `parseLMStudioModelrawModel: LLMInstanceInfo | LLMInfo` → `ModelInfo`

**Key Imports:** `axios`, `../../../shared/cost`, `@lmstudio/sdk`, `@roo-code/types`, `./modelCache`

---

### src\api\providers\fetchers\modelCache.ts
**Purpose:** Manages caching of model data using file system and memory.

**Exported Functions:**
- `writeModelsrouter: RouterName, data: ModelRecord` → `Promise<void>`
- `readModelsrouter: RouterName` → `Promise<ModelRecord | undefined>`
- `getModelsFromCacheoptions: GetModelsOptions` → `Promise<ModelRecord | undefined>`
- `flushModelsrouter: RouterName` → `Promise<void>`

**Key Imports:** `path`, `fs`, `NodeCache`, `@roo-code/types`, `../../../utils/safeWriteJson`

---

### src\api\providers\fetchers\modelEndpointCache.ts
**Purpose:** Caches and retrieves model endpoint data using file system.

**Exported Functions:**
- `writeModelEndpointskey: string, data: ModelRecord` → `Promise<void>`
- `readModelEndpointskey: string` → `Promise<ModelRecord | undefined>`
- `getModelEndpoints{ router: RouterName, modelId?: string, endpoint?: string }` → `Promise<ModelRecord | undefined>`

**Key Imports:** `path`, `fs`, `NodeCache`, `../../../utils/safeWriteJson`, `sanitize`

---

### src\api\providers\fetchers\ollama.ts
**Purpose:** Fetches and parses models from the Ollama API.

**Exported Types:**
- `type OllamaModel`: details, digest, model, modified_at, name
- `type OllamaModelInfoResponse`: modelfile, parameters, template, details, model_info

**Key Imports:** `axios`, `@roo-code/types`, `zod`

---

### src\api\providers\fetchers\openrouter.ts
**Purpose:** Retrieves and structures OpenRouter model information.

**Exported Types:**
- `type OpenRouterBaseModel`: name, description, context_length, max_completion_tokens, pricing
- `type OpenRouterModel`: id, architecture, top_provider, supported_parameters, name

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../../../shared/api`, `../../../shared/cost`

---

### src\api\providers\fetchers\requesty.ts
**Purpose:** Fetches model information from the Requesty API.

**Exported Functions:**
- `getRequestyModelsbaseUrl?: string, apiKey?: string` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `@roo-code/types`, `../../../shared/cost`, `../../../shared/utils/requesty`

---

### src\api\providers\fetchers\unbound.ts
**Purpose:** Fetches model information from the Unbound API.

**Exported Functions:**
- `getUnboundModelsapiKey?: string | null` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `@roo-code/types`

---

### src\api\providers\fetchers\vercel-ai-gateway.ts
**Purpose:** Retrieves and structures Vercel AI Gateway model data.

**Exported Types:**
- `type VercelAiGatewayModel`: id, object, created, owned_by, name

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../../../shared/api`, `../../../shared/cost`

---

### src\api\providers\fireworks.ts
**Purpose:** Provides a handler for interacting with the Fireworks API.

**Exported Types:**
- `class FireworksHandler`: constructor

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\providers\gemini.ts
**Purpose:** Handles interactions with the Google Gemini API.

**Exported Types:**
- `class GeminiHandler`: constructor, await, getModel, calculateCost

**Key Imports:** `@google/genai`, `@roo-code/types`, `../../shared/api`, `../../shared/safeJsonParse`

---

### src\api\providers\glama.ts
**Purpose:** Provides a Glama API handler for processing and generating messages.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`

**Exported Types:**
- `class GlamaHandler`: options, baseURL, apiKey, modelId

**Key Imports:** `@anthropic-ai/sdk`, `axios`, `openai`, `@roo-code/types`, `../../shared/api`

---

### src\api\providers\groq.ts
**Purpose:** Implements a Groq API handler for processing and generating messages.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`

**Exported Types:**
- `class GroqHandler`: providerName, baseURL, apiKey, defaultProviderModelId
- `interface GroqUsage`: prompt_tokens_details, completion_tokens, prompt_tokens

**Key Imports:** `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/openai-format`, `../../shared/cost`

---

### src\api\providers\huggingface.ts
**Purpose:** Provides a Hugging Face API handler for processing and generating messages.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `fetchModels()` → `Promise<void>`
- `getModel()` → `any`

**Exported Types:**
- `class HuggingFaceHandler`: client, options, modelCache, providerName

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `../../shared/api`, `../transform/stream`, `../transform/openai-format`

---

### src\api\providers\human-relay.ts
**Purpose:** Enables human relay interaction for message processing and generation.

**Exported Functions:**
- `countTokens(_content: Array<Anthropic.Messages.ContentBlockParam>)` → `Promise<number>`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`

**Exported Types:**
- `class HumanRelayHandler`

**Key Imports:** `@anthropic-ai/sdk`, `vscode`, `../../utils/commands`, `../transform/stream`, `../index`

---

### src\api\providers\index.ts
**Purpose:** Exports all API provider handlers for various AI services.

---

### src\api\providers\io-intelligence.ts
**Purpose:** Provides an IO Intelligence API handler for message processing.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `getModel()` → `any`

**Exported Types:**
- `class IOIntelligenceHandler`: providerName, baseURL, defaultProviderModelId, providerModels

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\providers\lite-llm.ts
**Purpose:** Handles LiteLLM API requests for various LLM providers.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, message` → `ApiStream`

**Exported Types:**
- `class LiteLLMHandler`: options, name, baseURL, apiKey

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../../shared/cost`, `../../shared/api`

---

### src\api\providers\lm-studio.ts
**Purpose:** Provides an LM Studio API handler for processing messages.

**Exported Functions:**
- `getLmStudioModels()` → `Promise<ModelInfo[] | undefined>`
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStre`

**Exported Types:**
- `class LmStudioHandler`: options, client, providerName

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `axios`, `@roo-code/types`, `../../shared/api`

---

### src\api\providers\mistral.ts
**Purpose:** Implements a Mistral API handler for processing and generating messages.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`
- `getModel()` → `any`

**Exported Types:**
- `class MistralHandler`: options, client

**Key Imports:** `@anthropic-ai/sdk`, `@mistralai/mistralai`, `@roo-code/types`, `../../shared/api`, `../transform/mistral-format`

---

### src\api\providers\moonshot.ts
**Purpose:** Provides a Moonshot API handler extending OpenAI's functionality.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `getModel()` → `any`

**Exported Types:**
- `class MoonshotHandler`

**Key Imports:** `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`, `./openai`

---

### src\api\providers\native-ollama.ts
**Purpose:** Provides a native Ollama API handler for message processing.

**Exported Functions:**
- `convertToOllamaMessagesanthropicMessages: Anthropic.Messages.MessageParam[]` → `Message[]`
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`
- `fetchModel()` → `Promise<ModelInfo | undefined>`

**Exported Types:**
- `interface OllamaChatOptions`: temperature, num_ctx

**Key Imports:** `@anthropic-ai/sdk`, `ollama`, `@roo-code/types`, `../transform/stream`, `./base-provider`, `./fetchers/ollama`

---

### src\api\providers\ollama.ts
**Purpose:** Provides an Ollama API handler for processing and generating messages.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`

**Exported Types:**
- `class OllamaHandler`: options, client, providerName

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/openai-format`

---

### src\api\providers\openai-native.ts
**Purpose:** Implements an OpenAI native API handler for message processing.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`
- `getModel()` → `any`

**Exported Types:**
- `type OpenAiNativeModel`
- `class OpenAiNativeHandler`: options, client, lastResponseId, responseIdPromise

**Exported Constants:**
- `GPT5_MODEL_PREFIX` = `"gpt-5"`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../../shared/cost`

---

### src\api\providers\openai.ts
**Purpose:** Provides an OpenAI API handler for processing and generating messages.

**Exported Functions:**
- `getOpenAiModels()` → `Promise<ModelInfo[] | undefined>`
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`
- `getModel()` → `any`

**Exported Types:**
- `class OpenAiHandler`: options, client, providerName

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `axios`, `@roo-code/types`, `../../shared/api`, `../../utils/xml-matcher`

---

### src\api\providers\openrouter.ts
**Purpose:** Provides an OpenRouter API handler for processing and generating messages.

**Exported Functions:**
- `constructor(options: ApiHandlerOptions)` → `void`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`
- `fetchModel()` → `Promise<ModelRecord | undefined>`
- `getModel()` → `any`
- `completePrompt(prompt: string, modelId: string, options: any)` → `Promise<any>`

**Exported Types:**
- `interface ImageGenerationResponse`: choices, error

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/openai-format`

---

### src\api\providers\qwen-code.ts
**Purpose:** Manages Qwen code model interactions, handling authentication and requests.

**Exported Types:**
- `interface QwenOAuthCredentials`: access_token, refresh_token, token_type, expiry_date, resource_url?
- `interface QwenCodeHandlerOptions`: qwenCodeOauthPath?

**Exported Constants:**
- `QWEN_OAUTH_BASE_URL` = `"https://chat.qwen.ai"`
- `QWEN_OAUTH_TOKEN_ENDPOINT` = `"https://chat.qwen.ai/api/v1/oauth2/token"`
- `QWEN_OAUTH_CLIENT_ID` = `"f0304373b74a44d2b584a3fb70ca9e56"`
- `QWEN_DIR` = `".qwen"`
- `QWEN_CREDENTIAL_FILENAME` = `"oauth_creds.json"`

**Key Imports:** `node:fs`, `@anthropic-ai/sdk`, `openai`, `node:os`, `node:path`

---

### src\api\providers\requesty.ts
**Purpose:** Provides a handler for interacting with the Requesty API for language models.

**Exported Types:**
- `interface RequestyUsage`: prompt_tokens_details?, total_cost?
- `type RequestyChatCompletionParams`: requesty?, thinking?
- `class RequestyHandler`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/openai-format`

---

### src\api\providers\roo.ts
**Purpose:** Manages interactions with the Roo Code Cloud provider for language models.

**Exported Types:**
- `class RooHandler`: authStateListener?

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `@roo-code/cloud`, `../../shared/api`

---

### src\api\providers\router-provider.ts
**Purpose:** Abstract class providing a base for routing requests to different providers.

**Exported Types:**
- `type RouterProviderOptions`: name, baseURL, apiKey?, modelId?, defaultModelId, defaultModelInfo, options
- `class RouterProvider`: options, name, models, modelId?, defaultModelId, defaultModelInfo, client

**Key Imports:** `openai`, `@roo-code/types`, `../../shared/api`, `./base-provider`, `./fetchers/modelCache`

---

### src\api\providers\sambanova.ts
**Purpose:** Implements a handler for interacting with the SambaNova language model API.

**Exported Types:**
- `class SambaNovaHandler`

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\providers\unbound.ts
**Purpose:** Provides a handler for interacting with the Unbound language model API.

**Exported Types:**
- `interface UnboundUsage`: cache_creation_input_tokens?, cache_read_input_tokens?
- `type UnboundChatCompletionCreateParamsStreaming`: unbound_metadata
- `type UnboundChatCompletionCreateParamsNonStreaming`: unbound_metadata
- `class UnboundHandler`

**Exported Constants:**
- `ORIGIN_APP` = `"roo-code"`
- `DEFAULT_HEADERS` = `{"X-Unbound-Metadata":JSON.stringify({labels:[{key:"app",value:"roo-code"}])}`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\utils\__tests__\timeout-config.spec.ts
---

### src\api\providers\utils\openai-error-handler.ts
**Purpose:** Handles and transforms OpenAI client errors into user-friendly messages.

**Exported Functions:**
- `handleOpenAIErrorerror: unknown, providerName: string` → `Error`

**Key Imports:** `../../../i18n/setup`

---

### src\api\providers\utils\timeout-config.ts
**Purpose:** Retrieves and validates the API request timeout from VSCode configuration.

**Exported Functions:**
- `getApiRequestTimeout` → `number`

**Key Imports:** `vscode`

---

### src\api\providers\vercel-ai-gateway.ts
**Purpose:** Handles interactions with the Vercel AI Gateway for language models.

**Exported Types:**
- `interface VercelAiGatewayUsage`: cache_creation_input_tokens?, cost?
- `class VercelAiGatewayHandler`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\vertex.ts
**Purpose:** Provides a handler for interacting with the Vertex AI Gemini models.

**Exported Types:**
- `class VertexHandler`

**Key Imports:** `@roo-code/types`, `../../shared/api`, `../transform/model-params`, `./gemini`

---

### src\api\providers\vscode-lm.ts
**Purpose:** Manages interactions with VS Code's Language Model API for chat operations.

**Exported Functions:**
- `getVsCodeLmModels` → `any`

**Exported Types:**
- `class VsCodeLmHandler`

**Key Imports:** `@anthropic-ai/sdk`, `vscode`, `@roo-code/types`, `../../shared/api`, `../../shared/vsCodeSelectorUtils`

---

### src\api\providers\xai.ts
**Purpose:** Provides a handler for interacting with the xAI language model API.

**Exported Types:**
- `class XAIHandler`: options, client, providerName

**Exported Constants:**
- `XAI_DEFAULT_TEMPERATURE` = `0`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\zai.ts
**Purpose:** Handles interactions with the Z AI language model API.

**Exported Types:**
- `class ZAiHandler`

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\transform\__tests__\bedrock-converse-format.spec.ts
**Purpose:** Tests the conversion of messages to Bedrock Converse format.

**Key Imports:** `../bedrock-converse-format`, `@anthropic-ai/sdk`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\transform\__tests__\gemini-format.spec.ts
**Purpose:** Tests the conversion of Anthropic messages to Gemini format.

**Key Imports:** `@anthropic-ai/sdk`, `../gemini-format`

---

### src\api\transform\__tests__\image-cleaning.spec.ts
**Purpose:** Tests the removal of image blocks based on model capabilities.

**Key Imports:** `@roo-code/types`, `../../index`, `../../../core/task-persistence/apiMessages`, `../image-cleaning`

---

### src\api\transform\__tests__\mistral-format.spec.ts
**Purpose:** Tests the conversion of Anthropic messages to Mistral format.

**Key Imports:** `@anthropic-ai/sdk`, `../mistral-format`

---

### src\api\transform\__tests__\model-params.spec.ts
**Purpose:** Tests the retrieval of model parameters based on settings.

**Key Imports:** `@roo-code/types`, `../model-params`, `../../../shared/api`

---

### src\api\transform\__tests__\openai-format.spec.ts
**Purpose:** Tests the conversion of Anthropic messages to OpenAI format.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `../openai-format`

---

### src\api\transform\__tests__\r1-format.spec.ts
**Purpose:** Tests the conversion of Anthropic messages to R1 format.

**Key Imports:** `../r1-format`, `@anthropic-ai/sdk`, `openai`

---

### src\api\transform\__tests__\reasoning.spec.ts
**Purpose:** Tests reasoning parameter retrieval for different providers.

**Key Imports:** `@roo-code/types`, `../reasoning`

---

### src\api\transform\__tests__\simple-format.spec.ts
**Purpose:** Tests the conversion of Anthropic messages to simple format.

**Key Imports:** `@anthropic-ai/sdk`, `../simple-format`

---

### src\api\transform\__tests__\stream.spec.ts
**Purpose:** Tests API stream chunk handling and usage scenarios.

**Key Imports:** `../stream`

---

### src\api\transform\__tests__\vscode-lm-format.spec.ts
**Purpose:** Tests conversion and extraction for VS Code language model formats.

**Key Imports:** `@anthropic-ai/sdk`, `vscode`, `../vscode-lm-format`

---

### src\api\transform\bedrock-converse-format.ts
**Purpose:** Converts Anthropic messages into Bedrock Converse format messages.

**Exported Functions:**
- `convertToBedrockConverseMessagesAnthropic.Messages.MessageParam[]` → `Message[]`

**Exported Types:**
- `interface BedrockMessageContent`: type, text?, source?, format?, s3Location?, toolUseId?, name?, input?, output?

**Key Imports:** `@anthropic-ai/sdk`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\transform\cache-strategy\__tests__\cache-strategy.spec.ts
**Functions:** `createMessageWithTokens`, `createMessage`, `logPlacements`, `mockResolvedValue`, `mockImplementation`, `await`

---

### src\api\transform\cache-strategy\base-strategy.ts
**Purpose:** Defines a base class for cache strategies with common functionalities.

**Exported Functions:**
- `determineOptimalCachePoints` → `CacheResult`

**Exported Types:**
- `class CacheStrategy`: config, systemTokenCount, determineOptimalCachePoints, initializeMessageGroups, calculateSystemTokens

**Key Imports:** `@anthropic-ai/sdk`, `@aws-sdk/client-bedrock-runtime`, `./types`

---

### src\api\transform\cache-strategy\multi-point-strategy.ts
**Purpose:** Implements a multi-point caching strategy for optimal cache point placement.

**Exported Functions:**
- `determineOptimalCachePoints()` → `CacheResult`

**Exported Types:**
- `class MultiPointStrategy`: config, systemTokenCount, determineOptimalCachePoints, meetsMinTokenThreshold, formatWithoutCachePoints

**Key Imports:** `@aws-sdk/client-bedrock-runtime`, `./base-strategy`, `./types`, `../../../utils/logging`

---

### src\api\transform\cache-strategy\types.ts
**Purpose:** Defines types for model information, cache points, and cache strategy results.

**Exported Types:**
- `interface ModelInfo`: maxTokens, contextWindow, supportsPromptCache, maxCachePoints, minTokensPerCachePoint
- `interface CachePoint`: type
- `interface CacheResult`: system, messages, messageCachePointPlacements
- `interface CachePointPlacement`: index, type, tokens

**Key Imports:** `@anthropic-ai/sdk`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\transform\caching\__tests__\anthropic.spec.ts
---

### src\api\transform\caching\__tests__\gemini.spec.ts
---

### src\api\transform\caching\__tests__\vercel-ai-gateway.spec.ts
---

### src\api\transform\caching\__tests__\vertex.spec.ts
---

### src\api\transform\caching\anthropic.ts
**Purpose:** Adds cache breakpoints to Anthropic messages for conversation caching.

**Exported Functions:**
- `addCacheBreakpointsstring, messages: OpenAI.Chat.ChatCompletionMessageParam[]` → `any`

**Key Imports:** `openai`

---

### src\api\transform\caching\gemini.ts
**Purpose:** Adds cache breakpoints to Gemini messages based on a specified frequency.

**Exported Functions:**
- `addCacheBreakpointsstring, messages: OpenAI.Chat.ChatCompletionMessageParam[], frequency: number = 10` → `any`

**Key Imports:** `openai`

---

### src\api\transform\caching\vercel-ai-gateway.ts
**Purpose:** Adds cache control to Vercel AI Gateway messages for caching.

**Exported Functions:**
- `addCacheBreakpointsstring, messages: OpenAI.Chat.ChatCompletionMessageParam[]` → `any`

**Key Imports:** `openai`

---

### src\api\transform\caching\vertex.ts
**Purpose:** Adds cache breakpoints to Vertex messages for conversation caching.

**Exported Functions:**
- `addCacheBreakpointsmessages: Anthropic.Messages.MessageParam[]` → `any`

**Key Imports:** `@anthropic-ai/sdk`

---

### src\api\transform\gemini-format.ts
**Purpose:** Converts Anthropic content to Gemini format for model compatibility.

**Exported Functions:**
- `convertAnthropicContentToGeminicontent: string | Anthropic.ContentBlockParam[]` → `Part[]`

**Key Imports:** `@anthropic-ai/sdk`, `@google/genai`

---

### src\api\transform\image-cleaning.ts
**Purpose:** Removes image blocks from messages if the API handler doesn't support them.

**Exported Functions:**
- `maybeRemoveImageBlocksmessages: ApiMessage[], apiHandler: ApiHandler` → `ApiMessage[]`

**Key Imports:** `../../core/task-persistence/apiMessages`, `../index`

---

### src\api\transform\mistral-format.ts
**Purpose:** Transforms Anthropic messages into Mistral message format.

**Exported Types:**
- `type MistralMessage`: role, content

**Key Imports:** `@anthropic-ai/sdk`, `@mistralai/mistralai/models/components/assistantmessage`, `@mistralai/mistralai/models/components/systemmessage`, `@mistralai/mistralai/models/components/toolmessage`, `@mistralai/mistralai/models/components/usermessage`

---

### src\api\transform\model-params.ts
**Purpose:** Generates model parameters based on provider settings and model information.

**Exported Functions:**
- `getModelParamsoptions: GetModelParamsOptions<T>` → `any`

**Exported Types:**
- `type GetModelParamsOptions`: format, modelId, model, settings, defaultTemperature
- `type BaseModelParams`: maxTokens, temperature, reasoningEffort, reasoningBudget, verbosity
- `type AnthropicModelParams`: format, reasoning
- `type OpenAiModelParams`: format, reasoning
- `type GeminiModelParams`: format, reasoning

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./reasoning`

---

### src\api\transform\openai-format.ts
**Purpose:** Transforms Anthropic messages into OpenAI's message format.

**Exported Functions:**
- `convertToOpenAiMessagesanthropicMessages: Anthropic.Messages.MessageParam[]` → `OpenAI.Chat.ChatCompletionMessageParam[]`

**Key Imports:** `@anthropic-ai/sdk`, `openai`

---

### src\api\transform\r1-format.ts
**Purpose:** Converts Anthropic messages to OpenAI format, merging consecutive messages.

**Exported Functions:**
- `convertToR1Formatmessages: AnthropicMessage[]` → `Message[]`

**Exported Types:**
- `type ContentPartText`
- `type ContentPartImage`
- `type UserMessage`
- `type AssistantMessage`
- `type Message`
- `type AnthropicMessage`

**Key Imports:** `@anthropic-ai/sdk`, `openai`

---

### src\api\transform\reasoning.ts
**Purpose:** Defines and retrieves reasoning parameters for various model providers.

**Exported Types:**
- `type OpenRouterReasoningParams`: effort?, max_tokens?, exclude?
- `type AnthropicReasoningParams`
- `type OpenAiReasoningParams`: reasoning_effort
- `type GeminiReasoningParams`
- `type GetModelReasoningOptions`: model, reasoningBudget, reasoningEffort, settings

**Exported Constants:**
- `getOpenRouterReasoning` = `function`
- `getAnthropicReasoning` = `function`
- `getOpenAiReasoning` = `function`

**Key Imports:** `@anthropic-ai/sdk/resources/beta`, `openai`, `@google/genai`, `@roo-code/types`, `../../shared/api`

---

### src\api\transform\simple-format.ts
**Purpose:** Converts Anthropic messages into a simplified string-based format.

**Exported Functions:**
- `convertToSimpleContentcontent: Anthropic.Messages.MessageParam["content"]` → `string`
- `convertToSimpleMessagesmessages: Anthropic.Messages.MessageParam[]` → `Array<{ role: "user" | "assistant"; content: string }>`

**Key Imports:** `@anthropic-ai/sdk`

---

### src\api\transform\stream.ts
**Purpose:** Defines types for streaming API responses, including chunks and errors.

**Exported Types:**
- `type ApiStream`
- `type ApiStreamChunk`
- `interface ApiStreamError`: type, error, message
- `interface ApiStreamTextChunk`: type, text
- `interface ApiStreamReasoningChunk`: type, text
- `interface ApiStreamUsageChunk`: type, inputTokens, outputTokens, cacheWriteTokens?, cacheReadTokens?, reasoningTokens?, totalCost?
- `interface ApiStreamGroundingChunk`: type, sources
- `interface GroundingSource`: title, url, snippet?

---

### src\api\transform\vscode-lm-format.ts
**Purpose:** Transforms Anthropic messages into VS Code Language Model chat messages.

**Exported Functions:**
- `convertToVsCodeLmMessagesanthropicMessages: Anthropic.Messages.MessageParam[]` → `vscode.LanguageModelChatMessage[]`
- `extractTextCountFromMessagemessage: vscode.LanguageModelChatMessage` → `number`

**Key Imports:** `@anthropic-ai/sdk`, `vscode`

---

### src\core\assistant-message\__tests__\AssistantMessageParser.spec.ts
**Purpose:** Tests the AssistantMessageParser for correct message parsing.

**Key Imports:** `../AssistantMessageParser`, `../parseAssistantMessage`, `../../../shared/tools`

---

### src\core\assistant-message\__tests__\parseAssistantMessage.spec.ts
**Purpose:** Tests parsing assistant messages with different parsing functions.

**Key Imports:** `../../../shared/tools`, `../parseAssistantMessage`, `../parseAssistantMessageV2`

---

### src\core\assistant-message\__tests__\parseAssistantMessageBenchmark.ts
**Purpose:** Benchmarks the performance of assistant message parsing functions.

**Key Imports:** `perf_hooks`, `../parseAssistantMessage`, `../parseAssistantMessageV2`

---

### src\core\assistant-message\AssistantMessageParser.ts
**Purpose:** Parses assistant messages, maintaining state for efficient chunk processing.

**Exported Types:**
- `class AssistantMessageParser`: contentBlocks, currentTextContent, currentToolUse, accumulator

**Key Imports:** `@roo-code/types`, `../../shared/tools`, `./parseAssistantMessage`

---

### src\core\assistant-message\index.ts
**Purpose:** Exports types and functions for assistant message parsing and presentation.

**Exported Types:**
- `type AssistantMessageContent`

**Key Imports:** `./parseAssistantMessage`, `./presentAssistantMessage`

---

### src\core\assistant-message\parseAssistantMessage.ts
**Purpose:** Parses assistant messages into structured content blocks.

**Exported Functions:**
- `parseAssistantMessageassistantMessage: string` → `AssistantMessageContent[]`

**Exported Types:**
- `type AssistantMessageContent`

**Key Imports:** `@roo-code/types`, `../../shared/tools`

---

### src\core\assistant-message\parseAssistantMessageV2.ts
**Purpose:** Efficiently parses assistant messages with text and tool usage blocks.

**Exported Functions:**
- `parseAssistantMessageV2assistantMessage: string` → `AssistantMessageContent[]`

**Exported Types:**
- `type AssistantMessageContent`

**Key Imports:** `@roo-code/types`, `../../shared/tools`

---

### src\core\assistant-message\presentAssistantMessage.ts
**Purpose:** Presents assistant messages, handling tools and approvals.

**Exported Functions:**
- `presentAssistantMessage` → ``
- `checkpointSaveAndMark` → ``
- `pushToolResult` → ``
- `askApproval` → ``
- `askFinishSubTaskApproval` → ``
- `handleError` → ``

**Key Imports:** `clone-deep`, `serialize-error`, `@roo-code/types`, `@roo-code/telemetry`, `../../shared/modes`, `../../shared/tools`, `../tools/fetchInstructionsTool`, `../tools/listFilesTool`, `../tools/readFileTool`, `../tools/simpleReadFileTool`, `@roo-code/types`, `../tools/writeToFileTool`, `../tools/multiApplyDiffTool`, `../tools/insertContentTool`, `../tools/searchAndReplaceTool`, `../tools/listCodeDefinitionNamesTool`, `../tools/searchFilesTool`, `../tools/browserActionTool`, `../tools/executeCommandTool`, `../tools/useMcpToolTool`, `../tools/accessMcpResourceTool`, `../tools/askFollowupQuestionTool`, `../tools/switchModeTool`

---

### src\core\checkpoints\__tests__\checkpoint.test.ts
**Purpose:** Tests checkpoint functionality, including save, restore, and diff operations.

**Key Imports:** `vitest`, `../../task/Task`, `../../webview/ClineProvider`, `../index`, `vscode`

---

### src\core\checkpoints\index.ts
**Purpose:** Manages checkpoint services for tasks, including saving and restoring.

**Exported Functions:**
- `getCheckpointServicetask: Task, { interval = 250, timeout = 15_000 }: { interval?: number; timeout?: number } = {}` → `any`
- `checkGitInstallation` → ``
- `checkpointSave` → ``
- `checkpointRestore` → ``
- `checkpointDiff` → ``
- `log` → ``

**Key Imports:** `p-wait-for`, `vscode`, `@roo-code/telemetry`, `../task/Task`, `../../utils/path`, `../../utils/git`, `../../i18n`, `../../shared/ExtensionMessage`, `../../shared/getApiMetrics`, `../../integrations/editor/DiffViewProvider`, `../../services/checkpoints`

---

### src\core\condense\__tests__\condense.spec.ts
**Purpose:** Tests conversation summarization functionality and token counting.

**Key Imports:** `Anthropic`, `@roo-code/telemetry`, `../../../api/providers/base-provider`, `../../task-persistence/apiMessages`, `../index`

---

### src\core\condense\__tests__\index.spec.ts
**Purpose:** Tests the logic for summarizing and retrieving messages.

**Key Imports:** `vitest`, `@roo-code/telemetry`, `../../../api`, `../../task-persistence/apiMessages`, `../../../api/transform/image-cleaning`, `../index`

---

### src\core\condense\index.ts
**Purpose:** Summarizes conversations to manage context and reduce token usage.

**Exported Functions:**
- `summarizeConversation` → ``
- `getMessagesSinceLastSummary` → ``
- `await` → ``

**Exported Constants:**
- `N_MESSAGES_TO_KEEP` = `3`
- `MIN_CONDENSE_THRESHOLD` = `5`
- `MAX_CONDENSE_THRESHOLD` = `100`

**Key Imports:** `Anthropic`, `@roo-code/telemetry`, `../../i18n`, `../../api`, `../task-persistence/apiMessages`, `../../api/transform/image-cleaning`

---

### src\core\config\__tests__\ContextProxy.spec.ts
---

### src\core\config\__tests__\CustomModesManager.exportImportSlugChange.spec.ts
---

### src\core\config\__tests__\CustomModesManager.spec.ts
---

### src\core\config\__tests__\CustomModesManager.yamlEdgeCases.spec.ts
**Functions:** `mockFsReadFile`

---

### src\core\config\__tests__\CustomModesSettings.spec.ts
---

### src\core\config\__tests__\importExport.spec.ts
---

### src\core\config\__tests__\ModeConfig.spec.ts
**Functions:** `validateCustomMode`

---

### src\core\config\__tests__\ProviderSettingsManager.spec.ts
---

### src\core\config\ContextProxy.ts
**Purpose:** Manages and provides access to extension context and settings.

**Exported Functions:**
- `isPassThroughStateKeykey: string` → `boolean`
- `getInstance` → `ContextProxy | undefined`
- `constructorcontext: vscode.ExtensionContext` → ``
- `isInitialized` → `boolean`
- `initialize` → `Promise<void>`
- `extensionUri` → `vscode.Uri`
- `extensionPath` → `string`
- `globalStorageUri` → `vscode.Uri`
- `logUri` → `vscode.Uri`
- `extension` → `any`
- `extensionMode` → `vscode.ExtensionMode`
- `getSecretkey: SecretStateKey` → `Promise<string | undefined>`
- `storeSecretkey: SecretStateKey, value: string` → `Promise<void>`
- `setProviderSettingssettings: ProviderSettings` → `Promise<void>`
- `setValuesvalues: Partial<GlobalState>` → `Promise<void>`
- `resetAllState` → `Promise<void>`

**Exported Types:**
- `class ContextProxy`: originalContext: vscode.ExtensionContext, stateCache: GlobalState, secretCache: SecretState, _isInitialized: boolean

**Exported Constants:**
- `PASS_THROUGH_STATE_KEYS` = `["taskHistory"]`

**Key Imports:** `vscode`, `zod`, `@roo-code/types`, `@roo-code/telemetry`, `../../utils/logging`

---

### src\core\config\CustomModesManager.ts
**Purpose:** Manages custom modes, handling import/export and settings changes.

**Exported Functions:**
- `constructorprivate readonly context: v` → ``
- `handleSettingsChangeevent: vscode.ConfigurationChangeEvent` → `Promise<void>`
- `handleRoomodesChangeuri: vscode.Uri` → `Promise<void>`

**Exported Types:**
- `interface RuleFile`: relativePath: string, content: string
- `interface ExportedModeConfig`: rulesFiles?: RuleFile[]
- `interface ImportData`: customModes: ExportedModeConfig[]
- `interface ExportResult`: success: boolean, yaml?: string, error?: string
- `interface ImportResult`: success: boolean, error?: string
- `class CustomModesManager`: disposables: vscode.Disposable[], isWriting: boolean, writeQueue: Array<() => Promise<void>>, cachedModes: ModeConfig[] | null, cachedAt: number

**Key Imports:** `vscode`, `path`, `fs/promises`, `yaml`, `@roo-code/types`, `../../utils/fs`

---

### src\core\config\importExport.ts
**Purpose:** Provides functions for importing and exporting settings configurations.

**Exported Functions:**
- `importSettingsFromPathfilePath: string, { providerSettingsManager, contextProxy, customModesManager }: ImportOptions` → `Promise<void>`
- `importSettingsdata: string, options: ImportOptions` → `Promise<void>`
- `importSettingsFromFileoptions: ImportOptions` → `Promise<void>`
- `exportSettingsoptions: ExportOptions` → `Promise<void>`
- `importSettingsWithFeedbackdata: string, options: ImportWithProviderOptions` → `Promise<void>`

**Exported Types:**
- `type ImportOptions`: providerSettingsManager: ProviderSettingsManager, contextProxy: ContextProxy, customModesManager: CustomModesManager
- `type ExportOptions`: providerSettingsManager: ProviderSettingsManager, contextProxy: ContextProxy
- `type ImportWithProviderOptions`: provider: { settingsImportedAt?: number, postStateToWebview: () => Promise<void> }

**Key Imports:** `../../utils/safeWriteJson`, `os`, `path`, `fs/promises`, `vscode`, `z`, `@roo-code/types`

---

### src\core\config\ProviderSettingsManager.ts
**Purpose:** Manages provider settings, including storage, import/export, and migrations.

**Exported Functions:**
- `constructorprivate readonly context: ExtensionContext` → ``
- `generateId` → `string`
- `initialize` → `Promise<void>`
- `migrateRateLimitSecondssettings: ProviderSettingsWithId` → `ProviderSettingsWithId`
- `migrateDiffSettingssettings: ProviderSettingsWithId` → `ProviderSettingsWithId`
- `migrateOpenAiHeaderssettings: ProviderSettingsWithId` → `ProviderSettingsWithId`
- `migrateConsecutiveMistakeLimitsettings: ProviderSettingsWithId` → `ProviderSettingsWithId`
- `migrateTodoListEnabledsettings: ProviderSettingsWithId` → `ProviderSettingsWithId`
- `deleteConfigid: string` → `Promise<void>`
- `hasConfigid: string` → `boolean`
- `setModeConfigmodeId: string, providerId: string` → `Promise<void>`
- `getModeConfigIdmodeId: string` → `string | undefined`
- `export` → `Promise<string>`
- `importdata: string` → `Promise<void>`
- `resetAllConfigs` → `Promise<void>`
- `secretsKeyid: string` → `string`
- `storeid: string, settings: ProviderSettings` → `Promise<void>`

**Exported Types:**
- `interface SyncCloudProfilesResult`: hasChanges: boolean, activeProfileChanged: boolean, activeProfileId: string
- `type ModelMigrations`: K in ProviderName]?: Record<string, string>

**Exported Constants:**
- `MODEL_MIGRATIONS` = `{ roo: { 'roo/code-supernova': 'roo/code-supernova-1-million' } }`

**Key Imports:** `vscode`, `zod`, `fast-deep-equal`, `@roo-code/types`, `@roo-code/telemetry`, `../../shared/modes`

---

### src\core\context-tracking\FileContextTracker.ts
**Purpose:** Tracks file operations to prevent stale context in the application.

**Exported Functions:**
- `constructorreadonly taskId: string` → `void`
- `setupFileWatcher` → `void`
- `trackFileContext` → `Promise<void>`
- `saveTaskMetadata` → `Promise<void>`
- `addFileToFileContextTracker` → `void`

**Exported Types:**
- `class FileContextTracker`: taskId, providerRef, fileWatcher

**Key Imports:** `../../utils/safeWriteJson`, `path`, `vscode`, `../../utils/storage`, `../../shared/globalFileNames`

---

### src\core\context-tracking\FileContextTrackerTypes.ts
**Purpose:** Defines types and schemas for file context metadata using Zod.

**Exported Types:**
- `type RecordSource`
- `type FileMetadataEntry`: path, record_state, record_source, roo_read_date, roo_edit_date
- `type TaskMetadata`: files_in_context

**Key Imports:** `z`

---

### src\core\context\context-management\__tests__\context-error-handling.test.ts
**Functions:** `status`

---

### src\core\context\context-management\context-error-handling.ts
**Purpose:** Detects context window exceeded errors from various API responses.

**Exported Functions:**
- `checkContextWindowExceededErrorerror: unknown` → `boolean`

**Key Imports:** `openai`

---

### src\core\diff\insert-groups.ts
**Purpose:** Inserts multiple groups of elements into an array at specified indices.

**Exported Functions:**
- `insertGroupsoriginal: string[], insertGroups: InsertGroup[]` → `string[]`

**Exported Types:**
- `interface InsertGroup`: index, elements

---

### src\core\diff\strategies\__tests__\multi-search-replace.spec.ts
**Functions:** `hello`, `helloWorld`, `example`, `test`, `one`, `two`, `three`, `four`, `five`, `getData`, `processUsers`, `handleItems`, `processData`, `sum`, `outer`, `toBe`, `constructor`, `getValue`, `method`

---

### src\core\diff\strategies\multi-file-search-replace.ts
**Purpose:** Implements multi-file search and replace diff strategy functionality.

**Exported Functions:**
- `getSimilarityoriginal: string, search: string` → `number`
- `fuzzySearchlines: string[], searchChunk: string, startIndex: number, endIndex: number` → `any`

**Key Imports:** `fastest-levenshtein`, `@roo-code/types`, `../../../integrations/misc/extract-text`, `../../../shared/tools`, `../../../utils/text-normalization`

---

### src\core\diff\strategies\multi-search-replace.ts
**Purpose:** Provides multi-search and replace diff strategy implementations.

**Exported Functions:**
- `getSimilarityoriginal: string, search: string` → `number`
- `fuzzySearchlines: string[], searchChunk: string, startIndex: number, endIndex: number` → `any`

**Key Imports:** `fastest-levenshtein`, `@roo-code/types`, `../../../integrations/misc/extract-text`, `../../../shared/tools`, `../../../utils/text-normalization`

---

### src\core\environment\__tests__\getEnvironmentDetails.spec.ts
---

### src\core\environment\getEnvironmentDetails.ts
**Purpose:** Retrieves environment details for a given Cline task.

**Exported Functions:**
- `getEnvironmentDetailscline: Task, includeFileDetails: boolean = false` → `Promise<string>`

**Key Imports:** `path`, `os`, `vscode`, `p-wait-for`, `delay`

---

### src\core\environment\reminder.ts
**Purpose:** Formats the reminder section as a markdown block.

**Exported Functions:**
- `formatReminderSectiontodoList?: TodoItem[]` → `string`

**Key Imports:** `@roo-code/types`

---

### src\core\ignore\__mocks__\RooIgnoreController.ts
**Functions:** `constructor`

---

### src\core\ignore\__tests__\RooIgnoreController.security.spec.ts
---

### src\core\ignore\__tests__\RooIgnoreController.spec.ts
---

### src\core\ignore\RooIgnoreController.ts
**Purpose:** Controls LLM access to files using .rooignore patterns.

**Exported Functions:**
- `constructorcwd: string` → `void`
- `initialize` → `Promise<void>`

**Exported Types:**
- `class RooIgnoreController`: cwd, ignoreInstance, rooIgnoreContent

**Exported Constants:**
- `LOCK_TEXT_SYMBOL` = `"\u{1F512}"`

**Key Imports:** `path`, `../../utils/fs`, `fs/promises`, `fs`, `ignore`, `vscode`

---

### src\core\mentions\__tests__\index.spec.ts
**Purpose:** Tests URL error handling for mention parsing functionality.

**Key Imports:** `vscode`, `../index`, `../../../services/browser/UrlContentFetcher`

---

### src\core\mentions\__tests__\processUserContentMentions.spec.ts
**Purpose:** Tests the processing of user content mentions with various parameters.

**Key Imports:** `../processUserContentMentions`, `../index`, `../../../services/browser/UrlContentFetcher`, `../../context-tracking/FileContextTracker`

---

### src\core\mentions\index.ts
**Purpose:** Handles mentions, including parsing and opening files or URLs.

**Exported Functions:**
- `getUrlErrorMessageerror: unknown` → `string`
- `openMentionmention: string, cwd: string` → `Promise<void>`
- `parseMentionstext: string, cwd: string` → `string[]`
- `getFileOrFolderContentfilePath: string, cwd: string, rooIgnoreController: RooIgnoreController` → `Promise<string | undefined>`
- `getWorkspaceProblemscwd: string` → `Promise<vscode.Diagnostic[]>`
- `getLatestTerminalOutputcwd: string` → `Promise<string | undefined>`

**Key Imports:** `fs/promises`, `path`, `vscode`, `../../shared/context-mentions`, `../../utils/git`

---

### src\core\mentions\processUserContentMentions.ts
**Purpose:** Processes mentions within user content, specifically task and feedback tags.

**Exported Functions:**
- `processUserContentMentions{ userContent, cwd, urlContentFetcher, fileContextTracker, rooIgnoreController, showRooIgnoredFiles, includeDiagnosticMessages, maxDiagnosticMessages, maxReadFileLine, }` → `Promise<void>`
- `shouldProcessMentionscontent: string` → `boolean`

**Key Imports:** `Anthropic`, `./index`, `../../services/browser/UrlContentFetcher`, `../context-tracking/FileContextTracker`

---

### src\core\message-queue\MessageQueueService.ts
**Purpose:** Manages a queue of messages with add, remove, and update functionalities.

**Exported Functions:**
- `constructor` → ``
- `addMessagetext: string, images?: string[]` → `QueuedMessage | undefined`
- `removeMessageid: string` → `boolean`
- `updateMessageid: string, text: string, images?: string[]` → `boolean`

**Exported Types:**
- `interface MessageQueueState`: messages: QueuedMessage[], isProcessing: boolean, isPaused: boolean
- `interface QueueEvents`: stateChanged: [messages: QueuedMessage[]]
- `class MessageQueueService`: _messages: QueuedMessage[], addMessage, removeMessage, updateMessage

**Key Imports:** `events`, `uuid`, `@roo-code/types`

---

### src\core\prompts\__tests__\add-custom-instructions.spec.ts
**Purpose:** Tests adding custom instructions to the system prompt.

**Key Imports:** `vscode`, `../system`, `../../../services/mcp/McpHub`, `../../../shared/modes`, `../utils/path`

---

### src\core\prompts\__tests__\custom-system-prompt.spec.ts
**Purpose:** Tests the custom system prompt functionality.

**Key Imports:** `../system`, `../../../shared/modes`, `vscode`, `fs/promises`, `./utils`

---

### src\core\prompts\__tests__\get-prompt-component.spec.ts
**Purpose:** Tests retrieval of prompt components based on custom mode prompts.

**Key Imports:** `@roo-code/types`, `../system`, `describe`, `it`, `expect`

---

### src\core\prompts\__tests__\responses-rooignore.spec.ts
**Purpose:** Tests the formatting of responses related to .rooignore files.

**Key Imports:** `../responses`, `../../ignore/RooIgnoreController`, `../../../utils/fs`, `fs/promises`, `./utils`

---

### src\core\prompts\__tests__\sections.spec.ts
**Purpose:** Tests the functionality of prompt sections and capabilities.

**Key Imports:** `../sections/custom-instructions`, `../sections/capabilities`, `../../../shared/tools`, `describe`, `it`, `expect`

---

### src\core\prompts\__tests__\system-prompt.spec.ts
**Purpose:** Tests the generation of the system prompt.

**Key Imports:** `vscode`, `@roo-code/types`, `../system`, `../../../services/mcp/McpHub`, `../../../shared/modes`, `../../../utils/path`

---

### src\core\prompts\__tests__\utils.ts
**Purpose:** Provides a utility function to convert file paths to POSIX format.

**Exported Functions:**
- `toPosixfilePath: PathLike | fs.FileHandle` → `string`

**Key Imports:** `fs/promises`, `PathLike`

---

### src\core\prompts\instructions\create-mcp-server.ts
**Purpose:** Generates instructions for creating and configuring MCP servers.

**Exported Functions:**
- `createMCPServerInstructionsmcpHub: McpHub | undefined, diffStrategy: DiffStrategy | undefined` → `Promise<string>`

**Key Imports:** `../../../services/mcp/McpHub`, `../../../shared/tools`

---

### src\core\prompts\instructions\create-mode.ts
**Purpose:** Provides instructions for creating and managing custom modes.

**Exported Functions:**
- `createModeInstructionscontext: vscode.ExtensionContext | undefined` → `Promise<string>`

**Key Imports:** `path`, `vscode`, `../../../shared/globalFileNames`

---

### src\core\prompts\instructions\instructions.ts
**Purpose:** Fetches instructions based on the provided text and details.

**Exported Functions:**
- `fetchInstructionstext: string, detail: InstructionsDetail` → `Promise<string>`

**Exported Types:**
- `interface InstructionsDetail`: mcpHub?: McpHub, diffStrategy?: DiffStrategy, context?: vscode.ExtensionContext

**Key Imports:** `./create-mcp-server`, `./create-mode`, `../../../services/mcp/McpHub`, `../../../shared/tools`, `vscode`

---

### src\core\prompts\responses.ts
**Purpose:** Defines various response formats for tool interactions and errors.

**Exported Constants:**
- `formatResponse` = `string`

**Key Imports:** `@anthropic-ai/sdk`, `path`, `diff`, `../ignore/RooIgnoreController`, `../protect/RooProtectedController`

---

### src\core\prompts\sections\__tests__\custom-instructions-global.spec.ts
**Purpose:** Tests global custom instructions and .roo file handling.

**Key Imports:** `* as path`, `../custom-instructions`

---

### src\core\prompts\sections\__tests__\custom-instructions-path-detection.spec.ts
**Purpose:** Tests custom instruction path detection logic for robustness.

**Key Imports:** `* as path`

---

### src\core\prompts\sections\__tests__\custom-instructions.spec.ts
**Purpose:** Tests custom instructions, mocking file system and path resolution.

**Key Imports:** `path`

---

### src\core\prompts\sections\__tests__\custom-system-prompt.spec.ts
**Purpose:** Tests loading and handling of custom system prompt files.

**Key Imports:** `* as vscode`, `path`, `fs/promises`, `../custom-system-prompt`

---

### src\core\prompts\sections\__tests__\objective.spec.ts
**Purpose:** Tests the objective section, focusing on codebase_search integration.

**Key Imports:** `../objective`, `../../../../services/code-index/manager`

---

### src\core\prompts\sections\__tests__\tool-use-guidelines.spec.ts
**Purpose:** Tests tool use guidelines, including codebase search enforcement.

**Key Imports:** `../tool-use-guidelines`, `../../../../services/code-index/manager`

---

### src\core\prompts\sections\capabilities.ts
**Purpose:** Generates a section describing the available capabilities and tools.

**Exported Functions:**
- `getCapabilitiesSectioncwd: string, supportsComputerUse: boolean, mcpHub?: McpHub, diffStrategy?: DiffStrategy, codeIndexManager?: CodeIndexManager` → `string`

**Key Imports:** `../../../shared/tools`, `../../../services/mcp/McpHub`, `../../../services/code-index/manager`

---

### src\core\prompts\sections\custom-instructions.ts
**Purpose:** Provides functions for handling custom instructions and file operations.

**Exported Functions:**
- `safeReadFilefilePath: string` → `Promise<string>`
- `directoryExistsdirPath: string` → `Promise<boolean>`
- `resolveDirectoryEntryentry: Dirent, dirPath: string, fileInfo: Array<{ originalPath: string; resolvedPath: string }>, depth: number` → `Promise<void>`
- `readTextFilesFromDirectorydirPath: string, fileInfo: Array<{ originalPath: string; resolvedPath: string }>, includeHiddenFiles?: boolean` → `Promise<string[]>`
- `formatDirectoryContentdirPath: string, fileInfo: Array<{ originalPath: string; resolvedPath: string }>, includeHiddenFiles?: boolean` → `Promise<string>`
- `loadRuleFilesrooDirectory: string, ruleType: string` → `Promise<string[]>`
- `loadAgentRulesFilerooDirectory: string, agentName: string` → `Promise<string>`
- `addCustomInstructionsinstructions: string[], customInstructions: string` → `string[]`
- `shouldIncludeRuleFilefileName: string` → `boolean`

**Exported Constants:**
- `MAX_DEPTH` = `5`

**Key Imports:** `fs`, `path`, `os`, `fs`, `@roo-code/types`, `../../../shared/language`, `../../../services/roo-config`

---

### src\core\prompts\sections\custom-system-prompt.ts
**Purpose:** Manages custom system prompts by interpolation and file operations.

**Exported Functions:**
- `interpolatePromptContentcontent: string, variables: PromptVariables` → `string`
- `safeReadFilefilePath: string` → `Promise<string>`
- `getSystemPromptFilePathcwd: string, mode: Mode` → `string`

**Exported Types:**
- `type PromptVariables`

**Key Imports:** `fs`, `path`, `../../../shared/modes`, `../../../utils/fs`

---

### src\core\prompts\sections\index.ts
**Purpose:** Exports all prompt section modules for easy access.

---

### src\core\prompts\sections\markdown-formatting.ts
**Purpose:** Generates a section enforcing markdown formatting rules.

**Exported Functions:**
- `markdownFormattingSection` → `string`

---

### src\core\prompts\sections\mcp-servers.ts
**Purpose:** Generates a section detailing connected MCP servers and their tools.

**Exported Functions:**
- `getMcpServersSectionmcpHub?: McpHub, diffStrategy?: DiffStrategy, enableMcpServerCreation?: boolean` → `Promise<string>`

**Key Imports:** `../../../shared/tools`, `../../../services/mcp/McpHub`

---

### src\core\prompts\sections\modes.ts
**Purpose:** Provides a section listing available modes and their descriptions.

**Exported Functions:**
- `getModesSectioncontext: vscode.ExtensionContext` → `Promise<string>`

**Key Imports:** `path`, `vscode`, `fs`, `../../../shared/modes`

---

### src\core\prompts\sections\objective.ts
**Purpose:** Generates the objective section outlining task execution steps.

**Exported Functions:**
- `getObjectiveSectioncodeIndexManager?: CodeIndexManager, experimentsConfig?: Record<string, boolean>` → `string`

**Key Imports:** `../../../services/code-index/manager`

---

### src\core\prompts\sections\rules.ts
**Purpose:** Provides editing instructions and general rules for tool usage.

**Exported Functions:**
- `getEditingInstructionsdiffStrategy?: DiffStrategy` → `string`
- `getRulesSectioncodeIndexManager?: CodeIndexManager, diffStrategy?: DiffStrategy` → `string`

**Key Imports:** `../../../shared/tools`, `../../../services/code-index/manager`

---

### src\core\prompts\sections\system-info.ts
**Purpose:** Provides system information like OS, shell, and workspace directory.

**Exported Functions:**
- `getSystemInfoSectioncwd: string` → `string`

**Key Imports:** `os`, `osName`, `../../../utils/shell`

---

### src\core\prompts\sections\tool-use-guidelines.ts
**Purpose:** Generates guidelines for tool usage, including codebase search emphasis.

**Exported Functions:**
- `getToolUseGuidelinesSectioncodeIndexManager?: CodeIndexManager` → `string`

**Key Imports:** `../../../services/code-index/manager`

---

### src\core\prompts\sections\tool-use.ts
**Purpose:** Defines the formatting and structure for tool use in prompts.

**Exported Functions:**
- `getSharedToolUseSection` → `string`

---

### src\core\prompts\system.ts
**Purpose:** Manages and generates system prompts for different modes and tools.

**Exported Functions:**
- `getPromptComponentcustomModePrompts: CustomModePrompts | undefined, mode: string` → `PromptComponent | undefined`
- `generatePromptcontext: vscode.ExtensionContext, cwd: string, supp` → `Promise<string>`

**Key Imports:** `* as vscode`, `* as os`, `@roo-code/types`, `../../shared/modes`, `../../services/code-index/manager`

---

### src\core\prompts\tools\__tests__\attempt-completion.spec.ts
---

### src\core\prompts\tools\__tests__\fetch-instructions.spec.ts
**Purpose:** Tests the generation of fetch instructions based on different conditions.

**Key Imports:** `../fetch-instructions`, `describe`, `it`, `expect`

---

### src\core\prompts\tools\__tests__\new-task.spec.ts
**Purpose:** Tests the new task description generation with and without todos.

**Key Imports:** `../new-task`, `../types`, `describe`, `it`, `expect`

---

### src\core\prompts\tools\access-mcp-resource.ts
**Purpose:** Provides the description for the access_mcp_resource tool.

**Exported Functions:**
- `getAccessMcpResourceDescriptionargs: ToolArgs` → `string | undefined`

**Key Imports:** `./types`

---

### src\core\prompts\tools\ask-followup-question.ts
**Purpose:** Provides the description for the ask_followup_question tool.

**Exported Functions:**
- `getAskFollowupQuestionDescription` → `string`

---

### src\core\prompts\tools\attempt-completion.ts
**Purpose:** Provides the description for the attempt_completion tool.

**Exported Functions:**
- `getAttemptCompletionDescriptionargs?: ToolArgs` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\browser-action.ts
**Purpose:** Provides the description for the browser_action tool.

**Exported Functions:**
- `getBrowserActionDescriptionargs: ToolArgs` → `string | undefined`

**Key Imports:** `./types`

---

### src\core\prompts\tools\codebase-search.ts
**Purpose:** Provides the description for the codebase_search tool.

**Exported Functions:**
- `getCodebaseSearchDescriptionargs: ToolArgs` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\execute-command.ts
**Purpose:** Provides the description for the execute_command tool.

**Exported Functions:**
- `getExecuteCommandDescriptionargs: ToolArgs` → `string | undefined`

**Key Imports:** `./types`

---

### src\core\prompts\tools\fetch-instructions.ts
**Purpose:** Generates descriptions for the fetch_instructions tool.

**Exported Functions:**
- `getFetchInstructionsDescription(enableMcpServerCreation?: boolean)` → `string`

---

### src\core\prompts\tools\generate-image.ts
**Purpose:** Provides a description for the generate_image tool.

**Exported Functions:**
- `getGenerateImageDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\index.ts
**Purpose:** Aggregates tool descriptions based on the current mode.

**Exported Functions:**
- `getToolDescriptionsForMode` → ``

**Key Imports:** `@roo-code/types`, `../../../shared/tools`, `../../../services/mcp/McpHub`, `../../../shared/modes`, `./types`

---

### src\core\prompts\tools\insert-content.ts
**Purpose:** Generates a description for the insert_content tool.

**Exported Functions:**
- `getInsertContentDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\list-code-definition-names.ts
**Purpose:** Provides a description for the list_code_definition_names tool.

**Exported Functions:**
- `getListCodeDefinitionNamesDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\list-files.ts
**Purpose:** Generates a description for the list_files tool.

**Exported Functions:**
- `getListFilesDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\new-task.ts
**Purpose:** Provides descriptions for the new_task tool.

**Exported Functions:**
- `getNewTaskDescription(args?: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\read-file.ts
**Purpose:** Generates a description for the read_file tool.

**Exported Functions:**
- `getReadFileDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\run-slash-command.ts
**Purpose:** Provides a description for the run_slash_command tool.

**Exported Functions:**
- `getRunSlashCommandDescription()` → `string`

---

### src\core\prompts\tools\search-and-replace.ts
**Purpose:** Generates a description for the search_and_replace tool.

**Exported Functions:**
- `getSearchAndReplaceDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\search-files.ts
**Purpose:** Provides a description for the search_files tool.

**Exported Functions:**
- `getSearchFilesDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\simple-read-file.ts
**Purpose:** Generates a description for the simple read_file tool.

**Exported Functions:**
- `getSimpleReadFileDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\switch-mode.ts
**Purpose:** Provides a description for the switch_mode tool.

**Exported Functions:**
- `getSwitchModeDescription()` → `string`

---

### src\core\prompts\tools\types.ts
**Purpose:** Defines the ToolArgs type used by various tools.

**Exported Types:**
- `type ToolArgs`: cwd, supportsComputerUse, diffStrategy, browserViewportSize, mcpHub

**Key Imports:** `../../../shared/tools`, `../../../services/mcp/McpHub`

---

### src\core\prompts\tools\update-todo-list.ts
**Purpose:** Generates a description for the update_todo_list tool.

**Exported Functions:**
- `getUpdateTodoListDescription(args?: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\use-mcp-tool.ts
**Purpose:** Provides a description for the use_mcp_tool.

**Exported Functions:**
- `getUseMcpToolDescription(args: ToolArgs)` → `string | undefined`

**Key Imports:** `./types`

---

### src\core\prompts\tools\write-to-file.ts
**Purpose:** Generates a description for the write_to_file tool.

**Exported Functions:**
- `getWriteToFileDescription(args: ToolArgs)` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\types.ts
**Purpose:** Defines settings passed to system prompt generation functions.

**Exported Types:**
- `interface SystemPromptSettings`: maxConcurrentFileReads, todoListEnabled, useAgentRules, newTaskRequireTodos

---

### src\core\protect\__tests__\RooProtectedController.spec.ts
**Purpose:** Tests the RooProtectedController's write protection functionality.

**Key Imports:** `path`, `../RooProtectedController`, `describe`, `beforeEach`, `it`, `expect`

---

### src\core\protect\RooProtectedController.ts
**Purpose:** Controls write access to Roo configuration files using protection patterns.

**Exported Types:**
- `class RooProtectedController`: cwd, ignoreInstance, isWriteProtected

**Exported Constants:**
- `SHIELD_SYMBOL` = `"\u{1F6E1}"`

**Key Imports:** `path`, `ignore`

---

### src\core\sliding-window\__tests__\sliding-window.spec.ts
**Purpose:** Tests the sliding window conversation truncation functionality.

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `@roo-code/telemetry`, `../../../api/providers/base-provider`, `../../task-persistence/apiMessages`, `../../condense`, `../index`

---

### src\core\sliding-window\index.ts
**Purpose:** Manages conversation truncation to fit within token limits.

**Exported Functions:**
- `estimateTokenCountcontent: Array<Anthropic.Messages.ContentBlockParam>,
	apiHandler: ApiHandler` → `Promise<number>`
- `truncateConversationmessages: ApiMessage[],
	maxTokens: number,
	apiHandler: ApiHandler,
	summarize: (messages: ApiMessage[], apiHandler: ApiHandler) => Promise<SummarizeResponse>,
	modelId?: string` → `Promise<ApiMessage[]>`
- `truncateConversationIfNeededmessages: ApiMessage[],
	maxTokens: number,
	apiHandler: ApiHandler,
	summarize: (messages: ApiMessage[], apiHandler: ApiHandler) => Promise<SummarizeResponse>,
	modelId?: string` → `Promise<ApiMessage[]>`

**Exported Constants:**
- `TOKEN_BUFFER_PERCENTAGE` = `0.1`

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/telemetry`, `../../api`, `../condense`, `../task-persistence/apiMessages`, `@roo-code/types`

---

### src\core\task-persistence\apiMessages.ts
**Purpose:** Manages reading and saving API messages for task persistence.

**Exported Types:**
- `type ApiMessage`: ts?: number, isSummary?: boolean

**Key Imports:** `safeWriteJson`, `path`, `fs/promises`, `fileExistsAtPath`, `GlobalFileNames`

---

### src\core\task-persistence\index.ts
**Purpose:** Exports modules for task persistence and data management.

**Key Imports:** `./apiMessages`, `./taskMessages`, `./taskMetadata`

---

### src\core\task-persistence\taskMessages.ts
**Purpose:** Reads and saves task messages using file system operations.

**Exported Functions:**
- `readTaskMessagesReadTaskMessagesOptions` → `Promise<ClineMessage[]>`
- `saveTaskMessagesSaveTaskMessagesOptions` → `Promise<void>`

**Exported Types:**
- `type ReadTaskMessagesOptions`: taskId: string, globalStoragePath: string
- `type SaveTaskMessagesOptions`: messages: ClineMessage[], taskId: string, globalStoragePath: string

**Key Imports:** `safeWriteJson`, `path`, `fs/promises`, `ClineMessage`, `fileExistsAtPath`, `GlobalFileNames`

---

### src\core\task-persistence\taskMetadata.ts
**Purpose:** Generates task metadata, including size and token usage.

**Exported Functions:**
- `taskMetadataTaskMetadataOptions` → `Promise<any>`

**Exported Types:**
- `type TaskMetadataOptions`: taskId: string, rootTaskId?: string, parentTaskId?: string, taskNumber: number

**Key Imports:** `NodeCache`, `get-folder-size`, `ClineMessage`, `HistoryItem`, `combineApiRequests`

---

### src\core\task\__tests__\AutoApprovalHandler.spec.ts
---

### src\core\task\__tests__\grounding-sources.test.ts
---

### src\core\task\__tests__\Task.dispose.test.ts
---

### src\core\task\__tests__\Task.spec.ts
**Functions:** `next`, `return`, `throw`

---

### src\core\task\AutoApprovalHandler.ts
**Purpose:** Handles auto-approval limits for requests and costs.

**Exported Types:**
- `interface AutoApprovalResult`: shouldProceed, requiresApproval, approvalType, approvalCount
- `class AutoApprovalHandler`: lastResetMessageIndex, consecutiveAutoApprovedRequestsCount, consecutiveAutoApprovedCost, checkAutoApprovalLimits

**Key Imports:** `@roo-code/types`, `../../shared/getApiMetrics`, `../../shared/WebviewMessage`

---

### src\core\task\Task.ts
**Purpose:** Manages tasks, including API interactions, state, and event handling.

**Exported Types:**
- `type TaskLike`: id, status, cwd, messages, metadata
- `type TaskMetadata`: taskId, modeSlug, startTime, endTime, status
- `type TaskEvents`: on, emit, off, eventNames, removeAllListeners
- `type ProviderSettings`: providerId, modelId, apiKey, apiUrl, apiProtocol
- `type TokenUsage`: inputTokens, outputTokens, totalTokens, cost
- `type ToolUsage`: toolName, inputTokens, outputTokens, cost
- `type ToolName`: name
- `type ContextCondense`: messages, tokenCount, summarize
- `type ClineMessage`: id, role, content, type, metadata
- `type ClineSay`: content, type, metadata
- `type ClineAsk`: content, type, metadata, options, id
- `type ToolProgressStatus`: toolName, status, message, progress
- `type HistoryItem`: id, messages, metadata, tokenUsage
- `type CreateTaskOptions`: modeSlug, cwd, initialMessages, providerSettings, taskMetadata
- `type RooCodeEventName`: TaskCreated, TaskUpdated, TaskAborted, TaskCompleted
- `type TelemetryEventName`: TaskCreated, TaskUpdated, TaskAborted, TaskCompleted
- `type TaskStatus`: idle, running, aborted, completed
- `type TodoItem`: text, checked
- `type DEFAULT_CONSECUTIVE_MISTAKE_LIMIT`
- `type getApiProtocol`
- `type getModelId`
- `type isIdleAsk`
- `type isInteractiveAsk`
- `type isResumableAsk`
- `type QueuedMessage`: message, resolve, reject

**Exported Constants:**
- `DEFAULT_CONSECUTIVE_MISTAKE_LIMIT` = `3`

**Key Imports:** `path`, `vscode`, `os`, `crypto`, `EventEmitter`, `@anthropic-ai/sdk`, `delay`, `pWaitFor`, `serialize-error`

---

### src\core\task\types.ts
**Purpose:** Defines types for task-related metadata and GPT-5 specific data.

**Exported Types:**
- `interface Gpt5Metadata`: previous_response_id?: string, instructions?: string, reasoning_summary?: string
- `interface ClineMessageWithMetadata`: metadata?: { gpt5?: Gpt5Metadata; [key: string]: any }

---

### src\core\tools\__tests__\applyDiffTool.experiment.spec.ts
---

### src\core\tools\__tests__\askFollowupQuestionTool.spec.ts
---

### src\core\tools\__tests__\attemptCompletionTool.spec.ts
---

### src\core\tools\__tests__\executeCommand.spec.ts
**Functions:** `describe`

---

### src\core\tools\__tests__\executeCommandTimeout.integration.spec.ts
---

### src\core\tools\__tests__\executeCommandTool.spec.ts
---

### src\core\tools\__tests__\generateImageTool.test.ts
---

### src\core\tools\__tests__\insertContentTool.spec.ts
**Functions:** `executeInsertContentTool`, `toPosix`, `initialize`, `validateAccess`, `mockImplementation`

---

### src\core\tools\__tests__\multiApplyDiffTool.spec.ts
**Functions:** `instance`

---

### src\core\tools\__tests__\newTaskTool.spec.ts
---

### src\core\tools\__tests__\readFileTool.spec.ts
**Purpose:** Tests the functionality of the read file tool.

**Exported Functions:**
- `initialize` → `any`
- `validateAccess` → `any`

**Key Imports:** `path`, `../../../integrations/misc/line-counter`, `../../../integrations/misc/read-lines`, `../../../integrations/misc/extract-text`, `../../../shared/tools`

---

### src\core\tools\__tests__\runSlashCommandTool.spec.ts
**Purpose:** Tests the execution of slash commands within the tool.

**Key Imports:** `vitest`, `../runSlashCommandTool`, `../../task/Task`, `../../prompts/responses`, `../../../services/command/commands`

---

### src\core\tools\__tests__\ToolRepetitionDetector.spec.ts
**Purpose:** Tests the detection of tool repetition to prevent infinite loops.

**Exported Functions:**
- `createToolUsename: string, displayName?: string, params: Record<string, string> = {}` → `ToolUse`

**Exported Types:**
- `class ToolRepetitionDetector`: check, reset, getRepetitionCount, toolRepetitionLimit

**Key Imports:** `@roo-code/types`, `../../../shared/tools`, `../ToolRepetitionDetector`

---

### src\core\tools\__tests__\updateTodoListTool.spec.ts
**Purpose:** Tests parsing of markdown checklists into todo items.

**Exported Functions:**
- `parseMarkdownChecklistmd: string` → `TodoItem[]`

**Key Imports:** `vitest`, `../updateTodoListTool`, `@roo-code/types`

---

### src\core\tools\__tests__\useMcpToolTool.spec.ts
**Purpose:** Tests the use of the MCP tool within the application.

**Key Imports:** `../useMcpToolTool`, `../../task/Task`, `../../../shared/tools`

---

### src\core\tools\__tests__\validateToolUse.spec.ts
**Purpose:** Tests tool usage validation against different modes.

**Key Imports:** `@roo-code/types`, `../../../shared/modes`, `../../../shared/tools`, `../validateToolUse`

---

### src\core\tools\__tests__\writeToFileTool.spec.ts
**Purpose:** Tests the write to file tool's functionality.

**Exported Functions:**
- `initialize` → `any`
- `validateAccess` → `any`

**Key Imports:** `path`, `../../../utils/fs`, `../../../integrations/editor/detect-omission`, `../../../utils/pathUtils`, `../../../utils/text-normalization`

---

### src\core\tools\accessMcpResourceTool.ts
**Purpose:** Implements a tool to access MCP resources within a task.

**Exported Functions:**
- `accessMcpResourceToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `ClineAskUseMcpServer`, `ToolUse`, `RemoveClosingTag`, `AskApproval`, `HandleError`

---

### src\core\tools\applyDiffTool.ts
**Purpose:** Applies diffs to files using the legacy applyDiffToolLegacy function.

**Exported Functions:**
- `applyDiffToolLegacycline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `path`, `fs/promises`, `TelemetryService`, `DEFAULT_WRITE_DELAY_MS`, `ClineSayTool`

---

### src\core\tools\askFollowupQuestionTool.ts
**Purpose:** Implements a tool to ask follow-up questions within a task.

**Exported Functions:**
- `askFollowupQuestionToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `Task`, `ToolUse`, `AskApproval`, `HandleError`, `PushToolResult`

---

### src\core\tools\attemptCompletionTool.ts
**Purpose:** Attempts code completion using the attemptCompletionTool function.

**Exported Functions:**
- `attemptCompletionToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag, toolDescription: ToolDescription, askFinishSubTaskApproval: AskFinishSubTaskApproval` → `Promise<void>`

**Key Imports:** `Anthropic`, `vscode`, `RooCodeEventName`, `TelemetryService`, `Task`

---

### src\core\tools\browserActionTool.ts
**Purpose:** Implements a tool for performing browser actions within a task.

**Exported Functions:**
- `browserActionToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `Task`, `ToolUse`, `AskApproval`, `HandleError`, `PushToolResult`

---

### src\core\tools\codebaseSearchTool.ts
**Purpose:** Provides a tool for searching the codebase within a task.

**Exported Functions:**
- `codebaseSearchToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `vscode`, `Task`, `CodeIndexManager`, `getWorkspacePath`, `formatResponse`

---

### src\core\tools\executeCommandTool.ts
**Purpose:** Executes shell commands using the executeCommandTool function.

**Exported Functions:**
- `executeCommandTooltask: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`
- `executeCommandtask: Task, command: string, cwd?: string, callbacks?: RooTerminalCallbacks` → `Promise<ToolResponse>`

**Key Imports:** `fs/promises`, `path`, `vscode`, `delay`, `CommandExecutionStatus`, `TelemetryService`, `Task`

---

### src\core\tools\fetchInstructionsTool.ts
**Purpose:** Fetches instructions using a tool and handles approval and errors.

**Exported Functions:**
- `fetchInstructionsToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult` → `Promise<void>`

**Key Imports:** `../task/Task`, `../../shared/ExtensionMessage`, `../../shared/tools`, `../prompts/responses`, `../prompts/instructions/instructions`

---

### src\core\tools\generateImageTool.ts
**Purpose:** Generates images using a tool, handling prompts and approvals.

**Exported Functions:**
- `generateImageToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Exported Constants:**
- `IMAGE_GENERATION_MODELS` = `["google/gemini-2.5-flash-image-preview"]`

**Key Imports:** `path`, `fs/promises`, `vscode`, `../task/Task`, `../../shared/tools`, `../../utils/fs`

---

### src\core\tools\helpers\imageHelpers.ts
**Purpose:** Provides image helpers for validation and processing image files.

**Exported Types:**
- `interface ImageValidationResult`: isValid: boolean, reason?: "size_limit" | "memory_limit" | "unsupported_model", notice?: string, s

**Exported Constants:**
- `DEFAULT_MAX_IMAGE_FILE_SIZE_MB` = `5`
- `DEFAULT_MAX_TOTAL_IMAGE_SIZE_MB` = `20`
- `SUPPORTED_IMAGE_FORMATS` = `[ ".png", ".jpg", ".jpeg", ".gif", ".webp", ".svg", ".bmp", ".ico", ".tiff", ".tif", ".avif" ]`
- `IMAGE_MIME_TYPES` = `{ ".png": "image/png", ".jpg": "image/jpeg", ".jpeg": "image/jpeg", ".gif": "image/gif", ".webp": "image/webp", ".svg": "image/svg+xml", ".bmp": "image/bmp", ".ico": "image/x-icon", ".tiff": "image/tiff", ".tif": "image/tiff", ".avif": "image/avif" }`

**Key Imports:** `path`, `fs/promises`, `../../../i18n`, `pretty-bytes`

---

### src\core\tools\insertContentTool.ts
**Purpose:** Inserts content into files using a tool with approval checks.

**Exported Functions:**
- `insertContentToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `delay`, `fs/promises`, `path`, `../../utils/path`, `../task/Task`, `../../shared/tools`

---

### src\core\tools\listCodeDefinitionNamesTool.ts
**Purpose:** Lists code definition names using a tool and handles workspace paths.

**Exported Functions:**
- `listCodeDefinitionNamesToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `path`, `fs/promises`, `../../shared/tools`, `../task/Task`, `../../shared/ExtensionMessage`, `../../utils/path`

---

### src\core\tools\listFilesTool.ts
**Purpose:** Implements the list_files tool for listing files in a directory.

**Exported Functions:**
- `listFilesToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `path`, `../task/Task`, `../../shared/ExtensionMessage`, `../../shared/tools`, `../../utils/path`, `../../utils/pathUtils`

---

### src\core\tools\multiApplyDiffTool.ts
**Purpose:** Applies multiple diff operations to files, managing their status.

**Exported Types:**
- `interface DiffOperation`: path: string, diff: Array<{ content: string; startLine?: number }>
- `interface OperationResult`: path: string, status: "pending" | "approved" | "denied" | "blocked" | "error", error?: string, result?: string
- `interface ParsedFile`: path: string, diff: ParsedDiff | ParsedDiff[]
- `interface ParsedDiff`: content: string, start_line?: string
- `interface ParsedXmlResult`: file: ParsedFile | ParsedFile[]

**Key Imports:** `path`, `fs/promises`, `../../shared/ExtensionMessage`, `../../utils/path`, `../task/Task`, `../../shared/tools`

---

### src\core\tools\newTaskTool.ts
**Purpose:** Creates new tasks using a tool, handling modes and parameters.

**Exported Functions:**
- `newTaskTooltask: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `vscode`, `@roo-code/types`, `../../shared/tools`, `../task/Task`, `../../shared/modes`, `../../shared/package`

---

### src\core\tools\readFileTool.ts
**Purpose:** Reads files using a tool, handling binary files and line counts.

**Exported Functions:**
- `getReadFileToolDescriptionblockName: string, blockParams: any` → `string`
- `readFileToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`
- `updateFileResultcline: Task, relPath: string, content: string, pushToolResult: PushToolResult` → `Promise<void>`

**Key Imports:** `path`, `isbinaryfile`, `../task/Task`, `../../shared/ExtensionMessage`, `../../shared/tools`, `../../i18n`, `../context-tracking/FileContextTrackerTypes`

---

### src\core\tools\runSlashCommandTool.ts
**Purpose:** Runs slash commands using a tool, checking experiment status.

**Exported Functions:**
- `runSlashCommandTooltask: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `../task/Task`, `../../shared/tools`, `../../shared/experiments`, `../../shared/experiments`

---

### src\core\tools\searchAndReplaceTool.ts
**Purpose:** Performs search and replace operations on files using a tool.

**Exported Functions:**
- `validateParamscline: Task, relPath: string | undefined, search: string | undefined, replace: string | undefined, pushToolResult: PushToolResult` → `Promise<boolean>`
- `searchAndReplaceToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`
- `escapeRegExptext: string` → `string`

**Key Imports:** `path`, `fs/promises`, `delay`, `../task/Task`, `../../shared/tools`, `../../shared/ExtensionMessage`, `../../utils/path`

---

### src\core\tools\searchFilesTool.ts
**Purpose:** Searches files using a tool, handling paths and regex patterns.

**Exported Functions:**
- `searchFilesToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `path`, `../task/Task`, `../../shared/ExtensionMessage`, `../../shared/tools`, `../../utils/path`, `../../utils/pathUtils`, `../../services/ripgrep`

---

### src\core\tools\simpleReadFileTool.ts
**Purpose:** Provides a simplified read file tool for single file reads.

**Exported Functions:**
- `simpleReadFileToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`
- `getSimpleReadFileToolDescriptionblockName: string, blockParams: any` → `string`

**Key Imports:** `path`, `isbinaryfile`, `../task/Task`, `../../shared/ExtensionMessage`, `../../shared/tools`, `../../i18n`, `../context-tracking/FileContextTrackerTypes`

---

### src\core\tools\switchModeTool.ts
**Purpose:** Switches modes using a tool, handling mode validation.

**Exported Functions:**
- `switchModeToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `delay`, `../task/Task`, `../../shared/tools`, `../../shared/modes`, `../../shared/modes`

---

### src\core\tools\ToolRepetitionDetector.ts
**Purpose:** Detects consecutive identical tool calls to prevent AI looping.

**Exported Functions:**
- `constructorlimit: number = 3` → `void`
- `checkcurrentToolCallBlock: ToolUse` → `{ allowExecution: boolean, askUser?: { messageKey: string, messageDetail: string } }`

**Exported Types:**
- `class ToolRepetitionDetector`: previousToolCallJson: string | null, consecutiveIdenticalToolCallCount: number, consecutiveIdenticalToolCallLimit: number

**Key Imports:** `../../shared/tools`, `../../i18n`

---

### src\core\tools\updateTodoListTool.ts
**Purpose:** Manages todo lists within tasks, adding, updating, and removing items.

**Exported Functions:**
- `addTodoToTaskcline: Task, content: string, status: TodoStatus = "pending", id?: string` → `TodoItem`
- `updateTodoStatusForTaskcline: Task, id: string, nextStatus: TodoStatus` → `boolean`
- `removeTodoFromTaskcline: Task, id: string` → `boolean`
- `getTodoListForTaskcline: Task` → `TodoItem[] | undefined`
- `setTodoListForTaskcline: Task, todoList: TodoItem[]` → `void`
- `restoreTodoListForTaskcline: Task, todoList: TodoItem[] | undefined` → `void`
- `todoListToMarkdowncline: Task` → `string`
- `normalizeStatusstatus: TodoStatus` → `TodoStatus`
- `parseMarkdownChecklistmarkdown: string` → `TodoItem[]`
- `setPendingTodoListcline: Task` → `void`
- `validateTodostodos: TodoItem[]` → `TodoItem[]`
- `updateTodoListToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Exported Types:**
- `type TodoItem`: id: string, content: string, status: TodoStatus
- `type TodoStatus`: pending, in_progress, completed

**Key Imports:** `../task/Task`, `../../shared/tools`, `../../shared/todo`, `clone-deep`, `crypto`

---

### src\core\tools\useMcpToolTool.ts
**Purpose:** Facilitates the use of MCP tools, handling requests and validations.

**Exported Functions:**
- `handlePartialRequestcline: Task, params: McpToolParams, removeClosingTag: RemoveClosingTag` → `Promise<void>`
- `validateParamscline: Task, params: McpToolParams, pushToolResult: PushToolResult` → `Promise<ValidationResult>`
- `validateToolExistscline: Task, serverName: string, toolName: string, pushToolResult: PushToolResult` → `Promise<boolean>`
- `sendExecutionStatuscline: Task, status: McpExecutionStatus, pushToolResult: PushToolResult` → `Promise<void>`
- `processToolContentcline: Task, toolName: string, toolArguments: string | undefined, pushToolResult: PushToolResult` → `Promise<void>`
- `executeToolAndProcessResultcline: Task, serverName: string, toolName: string, toolArguments: string | undefined, pushToolResult: PushToolResult, handleError: HandleError` → `Promise<void>`
- `useMcpToolToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Exported Types:**
- `interface McpToolParams`: server_name?: string, tool_name?: string, arguments?: string
- `type ValidationResult`: isValid: false, isValid: true, serverName: string, toolName: string

**Key Imports:** `../task/Task`, `../../shared/tools`, `../../shared/ExtensionMessage`, `@roo-code/types`, `../../i18n`

---

### src\core\tools\validateToolUse.ts
**Purpose:** Validates if a tool is allowed based on mode and configurations.

**Exported Functions:**
- `validateToolUsetoolName: ToolName, mode: Mode, customModes?: ModeConfig[], toolRequirements?: Record<string, boolean>, toolParams?: Record<string, unknown>` → `void`

**Key Imports:** `@roo-code/types`, `../../shared/modes`

---

### src\core\tools\writeToFileTool.ts
**Purpose:** Writes content to a file, handling approvals and errors.

**Exported Functions:**
- `writeToFileToolcline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag` → `Promise<void>`

**Key Imports:** `path`, `delay`, `vscode`, `fs/promises`, `../task/Task`

---

### src\core\webview\__tests__\checkpointRestoreHandler.spec.ts
**Purpose:** Tests the checkpoint restore handler functionality.

**Key Imports:** `vitest`, `../checkpointRestoreHandler`, `../../task-persistence`, `p-wait-for`, `vscode`

---

### src\core\webview\__tests__\ClineProvider.spec.ts
**Purpose:** Tests the ClineProvider webview component and its interactions.

**Exported Functions:**
- `delayFn` → `any`
- `getMessageHandler` → `any`
- `constructor` → `any`
- `instance` → `any`

**Key Imports:** `@anthropic-ai/sdk`, `vscode`, `axios`, `@roo-code/types`, `@roo-code/telemetry`

---

### src\core\webview\__tests__\ClineProvider.sticky-mode.spec.ts
**Purpose:** Tests the sticky mode functionality of the ClineProvider component.

**Exported Functions:**
- `instance` → `any`

**Key Imports:** `vscode`, `@roo-code/telemetry`, `../ClineProvider`, `../../config/ContextProxy`, `../../task/Task`

---

### src\core\webview\__tests__\messageEnhancer.test.ts
**Purpose:** Tests the messageEnhancer module for enhancing messages.

**Key Imports:** `@roo-code/types`, `@roo-code/telemetry`, `../messageEnhancer`, `../../../utils/single-completion-handler`, `../../config/ProviderSettingsManager`

---

### src\core\webview\__tests__\telemetrySettingsTracking.spec.ts
**Purpose:** Tests telemetry settings tracking within the webviewMessageHandler.

**Key Imports:** `vitest`, `@roo-code/telemetry`, `@roo-code/types`

---

### src\core\webview\__tests__\webviewMessageHandler.checkpoint.spec.ts
**Purpose:** Tests checkpoint operations within the webviewMessageHandler.

**Key Imports:** `vitest`, `../webviewMessageHandler`, `../../task-persistence`, `../checkpointRestoreHandler`

---

### src\core\webview\__tests__\webviewMessageHandler.delete.spec.ts
**Purpose:** Tests the delete functionality of the webviewMessageHandler.

**Key Imports:** `vitest`, `../webviewMessageHandler`, `vscode`, `../ClineProvider`

---

### src\core\webview\__tests__\webviewMessageHandler.edit.spec.ts
**Purpose:** Tests the edit message functionality of the webviewMessageHandler.

**Key Imports:** `vitest`, `../webviewMessageHandler`, `../ClineProvider`, `@roo-code/types`, `../../task-persistence/apiMessages`

---

### src\core\webview\__tests__\webviewMessageHandler.spec.ts
**Purpose:** Tests the webviewMessageHandler for handling various messages.

**Key Imports:** `../webviewMessageHandler`, `../ClineProvider`, `../../../api/providers/fetchers/modelCache`, `../../../shared/api`, `../../../i18n`

---

### src\core\webview\checkpointRestoreHandler.ts
**Purpose:** Handles checkpoint restoration for delete and edit operations.

**Exported Functions:**
- `handleCheckpointRestoreOperationconfig: CheckpointRestoreConfig` → `Promise<void>`

**Exported Types:**
- `interface CheckpointRestoreConfig`: provider, currentCline, messageTs, messageIndex, checkpoint

**Key Imports:** `../task/Task`, `./ClineProvider`, `../task-persistence`, `vscode`, `p-wait-for`, `../../i18n`

---

### src\core\webview\ClineProvider.ts
**Purpose:** Manages the Cline webview and task lifecycle.

**Exported Types:**
- `class ClineProvider`: onTaskStarted, onTaskCompleted, onTaskAborted, onTaskFocused

**Key Imports:** `os`, `path`, `fs`, `EventEmitter`, `@anthropic-ai/sdk`

---

### src\core\webview\generateSystemPrompt.ts
**Purpose:** Generates system prompts for the Cline webview.

**Exported Functions:**
- `generateSystemPromptprovider: ClineProvider, message: WebviewMessage` → `Promise<any>`

**Key Imports:** `vscode`, `../../shared/WebviewMessage`, `../../shared/modes`, `../../api`, `../../shared/experiments`, `../prompts/system`, `../diff/strategies/multi-search-replace`

---

### src\core\webview\getNonce.ts
**Purpose:** Generates a unique alphanumeric identifier (nonce).

**Exported Functions:**
- `getNonce` → `string`

---

### src\core\webview\getUri.ts
**Purpose:** Gets the webview URI for a given file or resource.

**Exported Functions:**
- `getUriwebview: Webview, extensionUri: Uri, pathList: string[]` → `Uri`

**Key Imports:** `vscode`

---

### src\core\webview\messageEnhancer.ts
**Purpose:** Enhances message prompts using AI, optionally including task history.

**Exported Types:**
- `interface MessageEnhancerOptions`: text, apiConfiguration, customSupportPrompts, listApiConfigMeta, enhancementApiConfigId
- `interface MessageEnhancerResult`: success, enhancedText, error
- `class MessageEnhancer`: enhanceMessage

**Key Imports:** `@roo-code/types`, `@roo-code/telemetry`, `../../shared/support-prompt`, `../../utils/single-completion-handler`, `../config/ProviderSettingsManager`, `./ClineProvider`

---

### src\core\webview\webviewMessageHandler.ts
**Purpose:** Handles messages received from the webview.

**Exported Functions:**
- `webviewMessageHandlerprovider: ClineProvider, message: WebviewMessage` → `Promise<void>`
- `getCurrentCwdprovider: ClineProvider` → `Promise<string>`
- `findMessageIndicesmessages: ClineMessage[], messageTs: number` → `{ messageIndex: number; apiIndex: number; } | undefined`
- `findFirstApiIndexAtOrAftermessages: ClineMessage[], messageIndex: number` → `number | undefined`
- `removeMessagesThisAndSubsequentmessages: ClineMessage[], messageIndex: number` → `void`

**Key Imports:** `../../utils/safeWriteJson`, `path`, `os`, `fs/promises`, `p-wait-for`

---

### src\extension.ts
**Purpose:** Activates and deactivates the RooCode extension in VS Code.

**Exported Functions:**
- `activatecontext: vscode.ExtensionContext` → `Promise<void>`
- `deactivate` → `Promise<void>`
- `postStateListenerevent: vscode.WebviewPanel` → `void`
- `debouncedReload` → `void`

**Key Imports:** `vscode`, `@dotenvx/dotenvx`, `path`, `@roo-code/types`, `@roo-code/cloud`

---

### src\extension\api.ts
**Purpose:** Provides an API for interacting with the RooCode extension.

**Exported Functions:**
- `startNewTaskoptions: CreateTaskOptions` → `Promise<ClineProvider | undefined>`
- `getCurrentTaskStack` → `ClineProvider[]`
- `clearCurrentTasktaskId: string` → `void`
- `cancelCurrentTask` → `Promise<void>`
- `cancelTasktaskId: string` → `Promise<void>`
- `sendMessagetaskId: string, message: string, options?: { stream?: boolean | undefined; } | undefined` → `Promise<void>`
- `pressPrimaryButtontaskId: string` → `Promise<void>`
- `pressSecondaryButtontaskId: string` → `Promise<void>`
- `isReady` → `boolean`
- `registerListeners` → `void`
- `outputChannelLog...args: unknown[]` → `void`
- `fileLog...args: unknown[]` → `Promise<void>`
- `setConfigurationsettings: Partial<RooCodeSettings>` → `Promise<void>`
- `createProfileprofile: ProviderSettingsEntry` → `Promise<void>`

**Exported Types:**
- `class API`: outputChannel, sidebarProvider, context, ipc, taskMap

**Key Imports:** `events`, `fs/promises`, `path`, `vscode`, `@roo-code/types`

---

### src\i18n\index.ts
**Purpose:** Manages internationalization and translation within the extension.

**Exported Functions:**
- `initializeI18nlanguage: string` → `void`
- `getCurrentLanguage` → `string`
- `changeLanguagelanguage: string` → `void`
- `tkey: string, options?: Record<string, any> | undefined` → `string`

**Key Imports:** `i18next`

---

### src\i18n\setup.ts
**Purpose:** Sets up and configures the i18next library for translations.

**Key Imports:** `i18next`

---

### src\integrations\claude-code\__tests__\message-filter.spec.ts
**Purpose:** Tests the message filter for Claude Code integration.

**Key Imports:** `@anthropic-ai/sdk`, `../message-filter`

---

### src\integrations\claude-code\__tests__\run.spec.ts
**Functions:** `createMockProcess`, `await`, `next`

---

### src\integrations\claude-code\message-filter.ts
**Purpose:** Filters messages for Claude Code, handling image block replacements.

**Exported Functions:**
- `filterMessagesForClaudeCodemessages: Anthropic.Messages.MessageParam[]` → `Anthropic.Messages.MessageParam[]`

**Key Imports:** `@anthropic-ai/sdk`

---

### src\integrations\claude-code\run.ts
**Purpose:** Runs Claude Code processes and handles their output.

**Exported Functions:**
- `runClaudeCodeoptions: ClaudeCodeOptions & { maxOutputTokens?: number; }` → `AsyncGenerator<ClaudeCodeMessage | string>`

**Key Imports:** `vscode`, `execa`, `readline`, `@roo-code/types`, `os`, `../../i18n`

---

### src\integrations\claude-code\types.ts
**Purpose:** Defines types for messages related to Claude Code integration.

**Exported Types:**
- `type ClaudeCodeMessage`

**Key Imports:** `@anthropic-ai/sdk`

---

### src\integrations\diagnostics\__tests__\diagnostics.spec.ts
---

### src\integrations\diagnostics\index.ts
**Purpose:** Provides functions to manage and format VS Code diagnostics.

**Exported Functions:**
- `getNewDiagnosticsoldDiagnostics: [vscode.Uri, vscode.Diagnostic[]][], newDiagnostics: [vscode.Uri, vscode.Diagnostic[]][]` → `[vscode.Uri, vscode.Diagnostic[]][]`
- `diagnosticsToProblemsString` → ``

**Key Imports:** `vscode`, `path`, `fast-deep-equal`

---

### src\integrations\editor\__tests__\detect-omission.spec.ts
**Functions:** `example`, `generateLongContent`

---

### src\integrations\editor\__tests__\DiffViewProvider.spec.ts
**Functions:** `label`, `tab`, `view`

---

### src\integrations\editor\__tests__\EditorUtils.spec.ts
**Functions:** `constructor`

---

### src\integrations\editor\DecorationController.ts
**Purpose:** Manages text editor decorations for highlighting code sections.

**Exported Types:**
- `type DecorationType`
- `class DecorationController`: decorationType, editor, ranges

**Key Imports:** `vscode`

---

### src\integrations\editor\detect-omission.ts
**Purpose:** Detects potential AI-generated code omissions in files.

**Exported Functions:**
- `detectCodeOmissionoriginalFileContent: string, newFileContent: string, predictedLineCount: number` → `boolean`

---

### src\integrations\editor\DiffViewProvider.ts
**Purpose:** Provides a diff view within VS Code for comparing file changes.

**Exported Types:**
- `class DiffViewProvider`: newProblemsMessage, userEdits, editType, isEditing, originalContent

**Exported Constants:**
- `DIFF_VIEW_URI_SCHEME` = `cline-diff`
- `DIFF_VIEW_LABEL_CHANGES` = `Original ↔ Roo's Changes`

**Key Imports:** `vscode`, `path`, `fs/promises`, `diff`, `strip-bom`

---

### src\integrations\editor\EditorUtils.ts
**Purpose:** Defines interfaces for editor context and diagnostic data.

**Exported Types:**
- `interface EffectiveRange`: range, text
- `interface DiagnosticData`: message, severity, code, source, range
- `interface EditorContext`: filePath, selectedText, startLine, endLine, diagnostics

**Key Imports:** `vscode`, `path`

---

### src\integrations\misc\__tests__\extract-text-from-xlsx.test.ts
---

### src\integrations\misc\__tests__\extract-text-large-files.spec.ts
**Functions:** `example`, `mockResolvedValue`, `toContain`

---

### src\integrations\misc\__tests__\extract-text.spec.ts
---

### src\integrations\misc\__tests__\line-counter.spec.ts
**Functions:** `mockImplementation`

---

### src\integrations\misc\__tests__\open-file.spec.ts
---

### src\integrations\misc\__tests__\performance\processCarriageReturns.benchmark.ts
**Functions:** `random`, `generateTestData`, `generateLongLineTestData`, `generateHighDensityCRData`, `getIterationCount`, `calculateStats`, `runPerformanceTest`, `runBaselineTest`, `runBenchmark`

---

### src\integrations\misc\__tests__\read-file-tool.spec.ts
**Functions:** `test`, `mockReturnValue`

---

### src\integrations\misc\__tests__\read-lines.spec.ts
**Functions:** `withTempFile`

---

### src\integrations\misc\export-markdown.ts
**Purpose:** Exports conversation history to a Markdown file.

**Exported Functions:**
- `downloadTaskdateTs: number, conversationHistory: Anthropic.MessageParam[]` → `Promise<void>`

**Key Imports:** `@anthropic-ai/sdk`, `os`, `path`, `vscode`

---

### src\integrations\misc\extract-text-from-xlsx.ts
**Purpose:** Extracts text content from XLSX files.

**Exported Functions:**
- `extractTextFromXLSXfilePathOrWorkbook: string | ExcelJS.Workbook` → `Promise<string>`

**Key Imports:** `exceljs`

---

### src\integrations\misc\extract-text.ts
**Purpose:** Extracts text from various file formats, including PDF and DOCX.

**Exported Functions:**
- `getSupportedBinaryFormats` → `any`
- `extractTextFromFilefilePath: string, fileExtension: string` → `Promise<string>`
- `addLineNumberstext: string` → `string`
- `everyLineHasLineNumberstext: string` → `boolean`
- `stripLineNumberstext: string` → `string`
- `truncateOutputtext: string, maxLength?: number` → `string`
- `applyRunLengthEncodingtext: string` → `string`
- `processCarriageReturnstext: string` → `string`
- `processBackspacestext: string` → `string`
- `processLineWithCarriageReturnsline: string` → `string`

**Key Imports:** `path`, `pdf-parse/lib/pdf-parse`, `mammoth`, `fs/promises`, `isbinaryfile`, `./extract-text-from-xlsx`, `./line-counter`, `./read-lines`

---

### src\integrations\misc\image-handler.ts
**Purpose:** Handles opening and saving images within VS Code.

**Exported Functions:**
- `openImagedataUriOrPath: string, options?: { values?: { action?: string } }` → `Promise<void>`
- `saveImage` → ``

**Key Imports:** `path`, `os`, `vscode`, `../../utils/path`, `../../i18n`

---

### src\integrations\misc\line-counter.ts
**Purpose:** Counts lines in a file efficiently using streams.

**Exported Functions:**
- `countFileLinesfilePath: string` → `Promise<number>`

**Key Imports:** `fs`, `fs`, `readline`

---

### src\integrations\misc\open-file.ts
**Purpose:** Opens files in VS Code, handling paths and optional content.

**Exported Functions:**
- `openFilefilePath: string, options: OpenFileOptions = {}` → `Promise<void>`

**Exported Types:**
- `interface OpenFileOptions`: create?: boolean, content?: string, line?: number

**Key Imports:** `path`, `os`, `vscode`, `../../utils/path`, `../../i18n`

---

### src\integrations\misc\process-images.ts
**Purpose:** Selects and processes images, returning data URLs for them.

**Exported Functions:**
- `selectImages()` → `Promise<string[]>`

**Key Imports:** `vscode`, `fs`, `path`

---

### src\integrations\misc\read-lines.ts
**Purpose:** Reads a range of lines from a file, handling start and end lines.

**Exported Functions:**
- `readLinesfilepath: string, endLine?: number, startLine?: number` → `Promise<string>`

**Key Imports:** `fs`

---

### src\integrations\terminal\__tests__\ExecaTerminal.spec.ts
---

### src\integrations\terminal\__tests__\ExecaTerminalProcess.spec.ts
---

### src\integrations\terminal\__tests__\setupTerminalTests.ts
**Functions:** `isPowerShellCoreAvailable`

---

### src\integrations\terminal\__tests__\streamUtils\bashStream.ts
**Functions:** `createBashCommandStream`

---

### src\integrations\terminal\__tests__\streamUtils\cmdStream.ts
**Functions:** `createCmdCommandStream`

---

### src\integrations\terminal\__tests__\streamUtils\index.ts
**Functions:** `isPowerShellCoreAvailable`, `getPlatform`, `isWindows`

---

### src\integrations\terminal\__tests__\streamUtils\mockStream.ts
**Functions:** `createBaseMockStream`, `createBashMockStream`, `createCmdMockStream`, `createPowerShellMockStream`, `createChunkedMockStream`

---

### src\integrations\terminal\__tests__\streamUtils\pwshStream.ts
**Functions:** `createPowerShellStream`

---

### src\integrations\terminal\__tests__\TerminalProcess.spec.ts
---

### src\integrations\terminal\__tests__\TerminalProcessExec.bash.spec.ts
**Purpose:** Tests terminal command execution using bash shell implementations.

**Exported Functions:**
- `createRealCommandStream` → ``
- `testTerminalCommand` → ``
- `constructor` → ``

**Key Imports:** `vscode`, `child_process`, `../types`, `../TerminalProcess`, `../Terminal`

---

### src\integrations\terminal\__tests__\TerminalProcessExec.cmd.spec.ts
**Purpose:** Tests terminal command execution using Windows cmd shell implementations.

**Exported Functions:**
- `testCmdCommand` → ``
- `onLine` → ``
- `constructor` → ``

**Key Imports:** `vscode`, `../types`, `../TerminalProcess`, `../Terminal`, `../TerminalRegistry`

---

### src\integrations\terminal\__tests__\TerminalProcessExec.common.ts
**Purpose:** Defines common test categories and parameters for terminal executions.

**Exported Constants:**
- `TEST_PURPOSES` = `object`
- `LARGE_OUTPUT_PARAMS` = `object`
- `TEST_TEXT` = `object`

---

### src\integrations\terminal\__tests__\TerminalProcessExec.pwsh.spec.ts
**Purpose:** Tests terminal command execution using PowerShell shell implementations.

**Exported Functions:**
- `testPowerShellCommand` → ``
- `onLine` → ``
- `constructor` → ``
- `foreach` → ``

**Key Imports:** `vscode`, `../types`, `../TerminalProcess`, `../Terminal`, `../TerminalRegistry`

---

### src\integrations\terminal\__tests__\TerminalProcessInterpretExitCode.spec.ts
**Purpose:** Tests the interpretation of exit codes from terminal processes.

**Key Imports:** `child_process`, `../TerminalProcess`

---

### src\integrations\terminal\__tests__\TerminalRegistry.spec.ts
**Purpose:** Tests the TerminalRegistry for creating and managing terminals.

**Key Imports:** `vscode`, `../Terminal`, `../TerminalRegistry`

---

### src\integrations\terminal\BaseTerminal.ts
**Purpose:** Defines a base class for terminal implementations, managing processes.

**Exported Types:**
- `class BaseTerminal`: provider: RooTerminalProvider, id: number, initialCwd: string, busy: boolean

**Key Imports:** `../misc/extract-text`, `@roo-code/types`, `./types`

---

### src\integrations\terminal\BaseTerminalProcess.ts
**Purpose:** Provides a base class for terminal processes, managing output and signals.

**Exported Types:**
- `class BaseTerminalProcess`: command: string, isHot: boolean, hotTimer: NodeJS.Timeout | null, isListening: boolean

**Key Imports:** `events`, `./types`

---

### src\integrations\terminal\ExecaTerminal.ts
**Purpose:** Implements a terminal using execa for running shell commands.

**Exported Types:**
- `class ExecaTerminal`: provider: RooTerminalProvider, id: number, initialCwd: string, busy: boolean

**Key Imports:** `./types`, `./BaseTerminal`, `./ExecaTerminalProcess`, `./mergePromise`

---

### src\integrations\terminal\ExecaTerminalProcess.ts
**Purpose:** Manages individual processes within an ExecaTerminal, handling execution.

**Exported Types:**
- `class ExecaTerminalProcess`: command: string, isHot: boolean, hotTimer: NodeJS.Timeout | null, isListening: boolean

**Key Imports:** `execa`, `ps-tree`, `process`, `./types`, `./BaseTerminalProcess`

---

### src\integrations\terminal\mergePromise.ts
**Purpose:** Merges a TerminalProcess with a Promise for terminal interaction.

**Exported Functions:**
- `mergePromiseprocess: RooTerminalProcess, promise: Promise<void>` → `RooTerminalProcessResultPromise`

**Key Imports:** `type { RooTerminalProcess, RooTerminalProcessResultPromise } from "./types"`

---

### src\integrations\terminal\ShellIntegrationManager.ts
**Purpose:** Manages shell integration, including temporary directory creation.

**Exported Types:**
- `class ShellIntegrationManager`: terminalTmpDirs: Map<number, string>

**Key Imports:** `import * as path from "path"`, `import * as vscode from "vscode"`

---

### src\integrations\terminal\Terminal.ts
**Purpose:** Provides a terminal implementation extending BaseTerminal functionality.

**Exported Types:**
- `class Terminal`: terminal: vscode.Terminal, cmdCounter: number, getCurrentWorkingDirectory(): string, isClosed(): boolean

**Key Imports:** `import * as vscode from "vscode"`, `import type { RooTerminalCallbacks, RooTerminalProcessResultPromise } from "./types"`, `import { BaseTerminal } from "./BaseTerminal"`, `import { ShellIntegrationManager } from "./ShellIntegrationManager"`, `import { mergePromise } from "./mergePromise"`

---

### src\integrations\terminal\TerminalProcess.ts
**Purpose:** Manages and controls terminal processes, handling commands execution.

**Exported Types:**
- `class TerminalProcess`: terminal: Terminal, run(command: string): Promise<void>, continue(): void, abort(): void

**Key Imports:** `import stripAnsi from "strip-ansi"`, `import * as vscode from "vscode"`, `import type { ExitCodeDetails } from "./types"`, `import { BaseTerminalProcess } from "./BaseTerminalProcess"`, `import { Terminal } from "./Terminal"`

---

### src\integrations\terminal\TerminalRegistry.ts
**Purpose:** Registers and manages terminal instances within the extension.

**Exported Types:**
- `class TerminalRegistry`: terminals: RooTerminal[], nextTerminalId: number, disposables: vscode.Disposable[]

**Key Imports:** `import * as vscode from "vscode"`, `import { RooTerminal, RooTerminalProvider } from "./types"`, `import { TerminalProcess } from "./TerminalProcess"`, `import { Terminal } from "./Terminal"`, `import { ExecaTerminal } from "./ExecaTerminal"`, `import { ShellIntegrationManager } from "./ShellIntegrationManager"`

---

### src\integrations\terminal\types.ts
**Purpose:** Defines terminal-related types, interfaces, and callback structures.

**Exported Types:**
- `interface RooTerminal`: provider: RooTerminalProvider, id: number, busy: boolean, running: boolean
- `interface RooTerminalCallbacks`: onLine: (line: string, process: RooTerminalProcess) => void, onCompleted: (output: string | undefined, process: RooTerminalProcess) => void, onShellExecutionStarted: (pid: number | undefined, process: RooTerminalProcess) => void
- `interface RooTerminalProcess`: command: string, isHot: boolean, run: (command: string) => Promise<void>, continue: () => void

**Key Imports:** `import EventEmitter from "events"`

---

### src\integrations\theme\getTheme.ts
**Purpose:** Fetches and parses VS Code theme information from extensions.

**Exported Functions:**
- `parseThemeStringthemeString: string | undefined` → `any`
- `getTheme` → ``
- `mergeJson` → ``
- `getExtensionUri` → ``

**Exported Types:**
- `type defaultThemes`: string

**Key Imports:** `vscode`, `path`, `fs/promises`, `monaco-vscode-textmate-theme-converter/lib/cjs`, `../../shared/package`

---

### src\integrations\workspace\__tests__\WorkspaceTracker.spec.ts
**Purpose:** Tests the WorkspaceTracker class for file path tracking.

**Key Imports:** `vitest`, `vscode`, `../WorkspaceTracker`, `../../../core/webview/ClineProvider`, `../../../services/glob/list-files`

---

### src\integrations\workspace\WorkspaceTracker.ts
**Purpose:** Tracks workspace files and manages file path updates.

**Exported Types:**
- `class WorkspaceTracker`: cwd, constructor, initializeFilePaths, registerListeners

**Key Imports:** `vscode`, `path`, `../../services/glob/list-files`, `../../core/webview/ClineProvider`, `../../utils/path`

---

### src\services\browser\__tests__\BrowserSession.spec.ts
**Purpose:** Tests the BrowserSession class for browser interactions.

**Key Imports:** `../BrowserSession`, `../browserDiscovery`

---

### src\services\browser\__tests__\UrlContentFetcher.spec.ts
**Purpose:** Tests the UrlContentFetcher class for fetching URL content.

**Key Imports:** `path`, `../UrlContentFetcher`

---

### src\services\browser\browserDiscovery.ts
**Purpose:** Discovers and checks Chrome browser instances on the network.

**Exported Functions:**
- `isPortOpenhost: string, port: number, timeout = 1000` → `Promise<boolean>`
- `tryChromeHostUrlchromeHostUrl: string` → `Promise<boolean>`
- `getDockerHostIP` → `Promise<string | null>`
- `scanNetworkForChrome` → ``
- `discoverChromeHostUrl` → ``

**Key Imports:** `net`, `axios`, `dns`

---

### src\services\browser\BrowserSession.ts
**Purpose:** Manages a browser session using Puppeteer for web interactions.

**Exported Types:**
- `class BrowserSession`: context, browser, page, currentMousePosition

**Key Imports:** `vscode`, `fs/promises`, `path`, `puppeteer-core`, `p-wait-for`, `delay`, `../../utils/fs`, `../../shared/ExtensionMessage`, `./browserDiscovery`

---

### src\services\browser\UrlContentFetcher.ts
**Purpose:** Fetches and processes content from a given URL using browser.

**Exported Types:**
- `class UrlContentFetcher`: context, browser, page

**Key Imports:** `vscode`, `fs/promises`, `path`, `puppeteer-core`, `cheerio`, `turndown`, `../../utils/fs`, `serialize-error`

---

### src\services\checkpoints\__tests__\excludes.spec.ts
---

### src\services\checkpoints\__tests__\ShadowCheckpointService.spec.ts
**Functions:** `initWorkspaceRepo`

---

### src\services\checkpoints\excludes.ts
**Purpose:** Provides functions to retrieve various file exclusion patterns.

**Exported Functions:**
- `getBuildArtifactPatterns` → `string[]`
- `getMediaFilePatterns` → `string[]`
- `getCacheFilePatterns` → `string[]`
- `getConfigFilePatterns` → `string[]`
- `getLargeDataFilePatterns` → `string[]`
- `getDatabaseFilePatterns` → `string[]`
- `getGeospatialPatterns` → `string[]`
- `getLogFilePatterns` → `string[]`
- `getLfsPatterns` → `string[]`
- `getExcludePatterns` → `Promise<string[]>`

**Key Imports:** `fs`, `path`, `../../utils/fs`

---

### src\services\checkpoints\index.ts
**Purpose:** Exports types and the RepoPerTaskCheckpointService class.

**Exported Types:**
- `type CheckpointServiceOptions`: taskId, workspaceDir, shadowDir, log?

**Key Imports:** `./types`, `./RepoPerTaskCheckpointService`

---

### src\services\checkpoints\RepoPerTaskCheckpointService.ts
**Purpose:** Creates and manages checkpoints for each task in a repository.

**Exported Functions:**
- `create{ taskId, workspaceDir, shadowDir, log = console.log }: CheckpointServiceOptions` → `RepoPerTaskCheckpointService`

**Exported Types:**
- `class RepoPerTaskCheckpointService`: taskId, checkpointsDir, workspaceDir, baseHash, isInitialized

**Key Imports:** `path`, `./types`, `./ShadowCheckpointService`

---

### src\services\checkpoints\ShadowCheckpointService.ts
**Purpose:** Provides an abstract class for shadow checkpoint services.

**Exported Types:**
- `class ShadowCheckpointService`: taskId, checkpointsDir, workspaceDir, baseHash, isInitialized

**Key Imports:** `fs`, `os`, `path`, `crypto`, `events`, `simple-git`, `p-wait-for`, `vscode`, `../../utils/fs`, `../../services/search/file-search`, `../../i18n`, `./types`, `./excludes`

---

### src\services\checkpoints\types.ts
**Purpose:** Defines types for checkpoint operations and events.

**Exported Types:**
- `type CheckpointResult`: commit
- `type CheckpointDiff`: paths, content
- `interface CheckpointServiceOptions`: taskId, workspaceDir, shadowDir, log?
- `interface CheckpointEventMap`: initialize, checkpoint, restore, error

**Key Imports:** `simple-git`

---

### src\services\code-index\__tests__\cache-manager.spec.ts
**Purpose:** Tests the CacheManager class for caching code index data.

**Key Imports:** `vitest`, `vscode`, `crypto`, `lodash.debounce`, `../cache-manager`

---

### src\services\code-index\__tests__\config-manager.spec.ts
**Purpose:** Tests the CodeIndexConfigManager for managing code index configurations.

**Key Imports:** `../config-manager`, `../interfaces/config`, `../../../core/config/ContextProxy`, `../../../shared/embeddingModels`

---

### src\services\code-index\__tests__\manager.spec.ts
**Purpose:** Tests the CodeIndexManager class for managing code indexing operations.

**Key Imports:** `../manager`, `../service-factory`, `vitest`, `path`

---

### src\services\code-index\__tests__\service-factory.spec.ts
**Purpose:** Tests the CodeIndexServiceFactory for creating code index services.

**Key Imports:** `vitest`, `../service-factory`, `../embedders/openai`, `../embedders/ollama`

---

### src\services\code-index\cache-manager.ts
**Purpose:** Manages the cache for code indexing, storing file hashes.

**Exported Types:**
- `class CacheManager`: cachePath, fileHashes, _debouncedSaveCache

**Key Imports:** `vscode`, `crypto`, `lodash.debounce`, `../../utils/safeWriteJson`, `@roo-code/telemetry`, `@roo-code/types`

---

### src\services\code-index\config-manager.ts
**Purpose:** Manages configuration and validation for code indexing features.

**Exported Types:**
- `class CodeIndexConfigManager`: codebaseIndexEnabled, embedderProvider, modelId, modelDimension, searchMinScore, searchMaxResults

**Key Imports:** `../../shared/api`, `../../core/config/ContextProxy`, `./interfaces/manager`, `./interfaces/config`, `./constants`, `../../shared/embeddingModels`

---

### src\services\code-index\constants\index.ts
**Purpose:** Defines constants used throughout the code indexing service.

**Exported Constants:**
- `MAX_BLOCK_CHARS` = `1000`
- `MIN_BLOCK_CHARS` = `50`
- `MIN_CHUNK_REMAINDER_CHARS` = `200`
- `MAX_CHARS_TOLERANCE_FACTOR` = `1.15`
- `DEFAULT_SEARCH_MIN_SCORE` = `CODEBASE_INDEX_DEFAULTS.DEFAULT_SEARCH_MIN_SCORE`
- `DEFAULT_MAX_SEARCH_RESULTS` = `CODEBASE_INDEX_DEFAULTS.DEFAULT_SEARCH_RESULTS`
- `QDRANT_CODE_BLOCK_NAMESPACE` = `"f47ac10b-58cc-4372-a567-0e02b2c3d479"`
- `MAX_FILE_SIZE_BYTES` = `1 * 1024 * 1024`
- `MAX_LIST_FILES_LIMIT_CODE_INDEX` = `50_000`
- `BATCH_SEGMENT_THRESHOLD` = `60`
- `MAX_BATCH_RETRIES` = `3`
- `INITIAL_RETRY_DELAY_MS` = `500`
- `PARSING_CONCURRENCY` = `10`
- `MAX_PENDING_BATCHES` = `20`
- `MAX_BATCH_TOKENS` = `100000`
- `MAX_ITEM_TOKENS` = `8191`
- `BATCH_PROCESSING_CONCURRENCY` = `10`
- `GEMINI_MAX_ITEM_TOKENS` = `2048`

**Key Imports:** `@roo-code/types`

---

### src\services\code-index\embedders\__tests__\gemini.spec.ts
**Purpose:** Tests GeminiEmbedder instantiation with different configurations.

**Key Imports:** `vitest`, `type { MockedClass } from "vitest"`, `GeminiEmbedder`, `OpenAICompatibleEmbedder`, `"@roo-code/telemetry"`

---

### src\services\code-index\embedders\__tests__\mistral.spec.ts
**Purpose:** Tests MistralEmbedder instantiation and API key validation.

**Key Imports:** `type { MockedClass } from "vitest"`, `MistralEmbedder`, `OpenAICompatibleEmbedder`, `"@roo-code/telemetry"`

---

### src\services\code-index\embedders\__tests__\ollama.spec.ts
**Purpose:** Tests the CodeIndexOllamaEmbedder for various scenarios.

**Key Imports:** `type { MockedFunction } from "vitest"`, `CodeIndexOllamaEmbedder`, `"@roo-code/telemetry"`, `"../../../../i18n"`

---

### src\services\code-index\embedders\__tests__\openai-compatible-rate-limit.spec.ts
**Purpose:** Tests OpenAICompatibleEmbedder's rate limiting and retry mechanisms.

**Key Imports:** `type { MockedClass, MockedFunction } from "vitest"`, `OpenAI`, `OpenAICompatibleEmbedder`, `"@roo-code/telemetry"`, `"../../../../i18n"`

---

### src\services\code-index\embedders\__tests__\openai-compatible.spec.ts
**Purpose:** Tests OpenAICompatibleEmbedder's embedding creation and error handling.

**Exported Functions:**
- `createMockResponseany` → `any`
- `createBase64Embeddingnumber` → `string`
- `expectEmbeddingValuesany, any` → `void`

**Key Imports:** `type { MockedClass, MockedFunction } from "vitest"`, `OpenAI`, `OpenAICompatibleEmbedder`, `"@roo-code/telemetry"`, `"../../../../i18n"`

---

### src\services\code-index\embedders\__tests__\openai.spec.ts
**Purpose:** Tests OpenAiEmbedder's embedding creation and error handling.

**Key Imports:** `type { MockedClass, MockedFunction } from "vitest"`, `OpenAI`, `OpenAiEmbedder`, `"@roo-code/telemetry"`, `"../../../../i18n"`

---

### src\services\code-index\embedders\__tests__\vercel-ai-gateway.spec.ts
**Purpose:** Tests VercelAiGatewayEmbedder instantiation with different models.

**Key Imports:** `VercelAiGatewayEmbedder`, `OpenAICompatibleEmbedder`, `"@roo-code/telemetry"`

---

### src\services\code-index\embedders\gemini.ts
**Purpose:** Implements Gemini embedder using OpenAI compatible embedder.

**Exported Types:**
- `class GeminiEmbedder`: openAICompatibleEmbedder, modelId

**Key Imports:** `./openai-compatible`, `../interfaces/embedder`, `../constants`, `../../../i18n`, `@roo-code/types`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\mistral.ts
**Purpose:** Implements Mistral embedder using OpenAI compatible embedder.

**Exported Types:**
- `class MistralEmbedder`: openAICompatibleEmbedder, modelId

**Key Imports:** `./openai-compatible`, `../interfaces/embedder`, `../constants`, `../../../i18n`, `@roo-code/types`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\ollama.ts
**Purpose:** Implements the IEmbedder interface using a local Ollama instance.

**Exported Types:**
- `class CodeIndexOllamaEmbedder`: baseUrl, defaultModelId

**Key Imports:** `../../../shared/api`, `../interfaces`, `../constants`, `../../../i18n`, `../shared/validation-helpers`, `@roo-code/telemetry`, `@roo-code/types`

---

### src\services\code-index\embedders\openai-compatible.ts
**Purpose:** Provides an OpenAI compatible embedder with batching and rate limiting.

**Exported Types:**
- `class OpenAICompatibleEmbedder`: embeddingsClient, defaultModelId, baseUrl, apiKey, isFullUrl, maxItemTokens

**Key Imports:** `openai`, `../interfaces/embedder`, `../constants`, `../../../shared/embeddingModels`, `../../../i18n`, `../shared/validation-helpers`, `@roo-code/types`, `@roo-code/telemetry`, `async-mutex`, `../../../api/providers/utils/openai-error-handler`

---

### src\services\code-index\embedders\openai.ts
**Purpose:** Implements OpenAI embedder with batching and rate limiting.

**Exported Types:**
- `class OpenAiEmbedder`: embeddingsClient, defaultModelId

**Key Imports:** `openai`, `../../../api/providers/openai-native`, `../../../shared/api`, `../interfaces`, `../constants`, `../../../shared/embeddingModels`, `../../../i18n`, `../shared/validation-helpers`, `@roo-code/types`, `@roo-code/telemetry`, `../../../api/providers/utils/openai-error-handler`

---

### src\services\code-index\embedders\vercel-ai-gateway.ts
**Purpose:** Implements Vercel AI Gateway embedder using OpenAI compatible embedder.

**Exported Types:**
- `class VercelAiGatewayEmbedder`: openAICompatibleEmbedder, modelId

**Key Imports:** `./openai-compatible`, `../interfaces/embedder`, `../constants`, `../../../i18n`, `@roo-code/types`, `@roo-code/telemetry`

---

### src\services\code-index\interfaces\cache.ts
**Purpose:** Defines the ICacheManager interface for managing file hashes.

**Exported Types:**
- `interface ICacheManager`: getHash(filePath: string): string | undefined, updateHash(filePath: string, hash: string): void, deleteHash(filePath: string): void, getAllHashes(): Record<string, string>

---

### src\services\code-index\interfaces\config.ts
**Purpose:** Defines configuration interfaces for code indexing features.

**Exported Types:**
- `interface CodeIndexConfig`: isConfigured: boolean, embedderProvider: EmbedderProvider, modelId?: string, modelDimension?: number, openAiOptions?: ApiHandlerOptions
- `type PreviousConfigSnapshot`: enabled: boolean, configured: boolean, embedderProvider: EmbedderProvider, modelId?: string, modelDimension?: number

**Key Imports:** `ApiHandlerOptions`, `EmbedderProvider`

---

### src\services\code-index\interfaces\embedder.ts
**Purpose:** Defines the IEmbedder interface and related types for embedding.

**Exported Types:**
- `interface IEmbedder`: createEmbeddings(texts: string[], model?: string): Promise<EmbeddingResponse>, validateConfiguration(): Promise<{ valid: boolean; error?: string }>, embedderInfo: EmbedderInfo
- `interface EmbeddingResponse`: embeddings: number[][], usage?: { promptTokens: number; totalTokens: number }
- `type AvailableEmbedders`
- `interface EmbedderInfo`: name: AvailableEmbedders

---

### src\services\code-index\interfaces\file-processor.ts
**Purpose:** Defines interfaces for code file parsing, directory scanning, and watching.

**Exported Types:**
- `interface ICodeParser`: parseFile(filePath: string, options?: { minBlockLines?: number; maxBlockLines?: number; content?: string; fileHash?: string }): Promise<CodeBlock[]>
- `interface IDirectoryScanner`: scanDirectory(directory: string, onError?: (error: Error) => void, onBlocksIndexed?: (indexedCount: number) => void, onFileParsed?: (fileBlockCount: number) => void): Promise<{ stats: { processed: number; skipped: number }; totalBlockCount: number }>
- `interface IFileWatcher`: initialize(): Promise<void>, onDidStartBatchProcessing: vscode.Event<string[], onDidFinishBatchProcessing: vscode.Event<BatchProcessingSummary>, onDidChangeFile: vscode.Event<vscode.FileEvent>

**Key Imports:** `vscode`, `PointStruct`

---

### src\services\code-index\interfaces\index.ts
**Purpose:** Exports all interfaces related to code indexing functionality.

**Key Imports:** `"./embedder"`, `"./vector-store"`, `"./file-processor"`, `"./manager"`

---

### src\services\code-index\interfaces\manager.ts
**Purpose:** Defines the ICodeIndexManager interface for managing code indexing.

**Exported Types:**
- `interface ICodeIndexManager`: onProgressUpdate: vscode.Event<{ systemStatus: IndexingState; fileStatuses: Record<string, string>; message?: string }>, state: IndexingState, isFeatureEnabled: boolean, isFeatureConfigured: boolean, loadConfiguration(): Promise<void>
- `type IndexingState`

**Key Imports:** `VectorStoreSearchResult`, `vscode`

---

### src\services\code-index\interfaces\vector-store.ts
**Purpose:** Defines interfaces for vector database clients and search results.

**Exported Types:**
- `type PointStruct`: id: string, vector: number[], payload: Record<string, any>
- `interface IVectorStore`: initialize(): Promise<boolean>, upsertPoints(points: PointStruct[]): Promise<void>, search(queryVector: number[], directoryPrefix?: string, minScore?: number, maxResults?: number): Promise<VectorStoreSearchResult[]>
- `type VectorStoreSearchResult`

---

### src\services\code-index\manager.ts
**Purpose:** Manages the code indexing process, including configuration and state.

**Exported Functions:**
- `constructorany` → `any`
- `onProgressUpdateany` → `any`
- `assertInitializedany` → `any`
- `getCurrentStatusany` → `any`

**Exported Types:**
- `class CodeIndexManager`: private _configManager: CodeIndexConfigManager | undefined, private readonly _stateManager: CodeIndexStateManager, private _serviceFactory: CodeIndexServiceFactory | undefined, private _orchestrator: CodeIndexOrchestrator | undefined, private _searchService: CodeIndexSearchService | undefined

**Key Imports:** `vscode`, `VectorStoreSearchResult`, `IndexingState`, `CodeIndexConfigManager`, `CodeIndexStateManager`

---

### src\services\code-index\orchestrator.ts
**Purpose:** Manages the code indexing workflow, coordinating different services.

**Exported Functions:**
- `handleFileParsedany` → `any`
- `handleBlocksIndexedany` → `any`
- `constructorany` → `any`

**Exported Types:**
- `class CodeIndexOrchestrator`: private _fileWatcherSubscriptions: vscode.Disposable[], private _isProcessing: boolean, private readonly configManager: CodeIndexConfigManager, private readonly stateManager: CodeIndexStateManager, private readonly workspacePath: string

**Key Imports:** `vscode`, `path`, `CodeIndexConfigManager`, `CodeIndexStateManager`, `IFileWatcher`

---

### src\services\code-index\processors\__tests__\file-watcher.spec.ts
---

### src\services\code-index\processors\__tests__\parser.spec.ts
**Functions:** `test`, `calculate`, `processItems`, `sum`, `f`, `g`, `mockCapture`, `constructor`, `add`

---

### src\services\code-index\processors\__tests__\parser.vb.spec.ts
---

### src\services\code-index\processors\__tests__\scanner.spec.ts
**Functions:** `main`

---

### src\services\code-index\processors\file-watcher.ts
**Purpose:** Implements the IFileWatcher interface for file system changes.

**Exported Functions:**
- `constructorany` → `any`

**Exported Types:**
- `class FileWatcher`: private ignoreInstance?: Ignore, private fileWatcher?: vscode.FileSystemWatcher, private ignoreController: RooIgnoreController, private accumulatedEvents: Map<string, { uri: vscode.Uri; type: "create" | "change" | "delete" }>, private batchProcessDebounceTimer?: NodeJS.Timeout

**Exported Constants:**
- `MAX_FILE_SIZE_BYTES` = `number`
- `BATCH_SEGMENT_THRESHOLD` = `number`
- `MAX_BATCH_RETRIES` = `number`
- `INITIAL_RETRY_DELAY_MS` = `number`

**Key Imports:** `vscode`, `"crypto"`, `RooIgnoreController`, `"uuid"`, `Ignore`

---

### src\services\code-index\processors\index.ts
**Purpose:** Exports code index processor modules for parsing and scanning.

**Key Imports:** `"./parser"`, `"./scanner"`, `"./file-watcher"`

---

### src\services\code-index\processors\parser.ts
**Purpose:** Parses code files into blocks using tree-sitter and markdown parsers.

**Exported Functions:**
- `finalizeChunk` → ``
- `createSegmentBlock` → ``
- `parseFilefilePath: string, options?: { content?: string; fileHash?: string; }` → `Promise<CodeBlock[]>`

**Exported Types:**
- `class CodeParser`: loadedParsers: LanguageParser, pendingLoads: Map<string, Promise<LanguageParser>>
- `interface ICodeParser`: parseFile(filePath: string, options?: { content?: string; fileHash?: string; }): Promise<CodeBlock[]>
- `type CodeBlock`: content: string, filePath: string, startLine: number, endLine: number, languageId: string

**Key Imports:** `"fs/promises"`, `"crypto"`, `"path"`, `"web-tree-sitter"`, `"../interfaces"`

---

### src\services\code-index\processors\scanner.ts
**Purpose:** Scans directories to identify and process code files for indexing.

**Exported Types:**
- `class DirectoryScanner`: batchSegmentThreshold: number, batchProcessingConcurrency: number, maxPendingBatches: number
- `interface IDirectoryScanner`: scanDirectory(directoryPath: string, options?: { concurrency?: number; }): Promise<void>

**Key Imports:** `"../../glob/list-files"`, `"ignore"`, `"../../../core/ignore/RooIgnoreController"`, `"fs/promises"`, `"path"`

---

### src\services\code-index\search-service.ts
**Purpose:** Provides a service for searching the code index using embeddings.

**Exported Types:**
- `class CodeIndexSearchService`: configManager: CodeIndexConfigManager, stateManager: CodeIndexStateManager, embedder: IEmbedder, vectorStore: IVectorStore

**Key Imports:** `"path"`, `"./interfaces"`, `"./interfaces/embedder"`, `"./interfaces/vector-store"`, `"./config-manager"`

---

### src\services\code-index\service-factory.ts
**Purpose:** Creates and configures dependencies for the code indexing service.

**Exported Types:**
- `class CodeIndexServiceFactory`: configManager: CodeIndexConfigManager, workspacePath: string, cacheManager: CacheManage

**Key Imports:** `"vscode"`, `"./embedders/openai"`, `"./embedders/ollama"`, `"./embedders/openai-compatible"`

---

### src\services\code-index\shared\__tests__\get-relative-path.spec.ts
---

### src\services\code-index\shared\__tests__\validation-helpers.spec.ts
---

### src\services\code-index\shared\get-relative-path.ts
**Purpose:** Generates normalized absolute and relative paths for code indexing.

**Exported Functions:**
- `generateNormalizedAbsolutePathfilePath: string, workspaceRoot: string` → `string`
- `generateRelativeFilePathnormalizedAbsolutePath: string, workspaceRoot: string` → `string`

**Key Imports:** `path`

---

### src\services\code-index\shared\supported-extensions.ts
**Purpose:** Defines supported file extensions and fallback chunking behavior.

**Exported Functions:**
- `shouldUseFallbackChunkingextension: string` → `boolean`

**Exported Constants:**
- `scannerExtensions` = `allExtensions`
- `fallbackExtensions` = `[ ".vb", ".scala", ".swift" ]`

**Key Imports:** `"../../tree-sitter"`

---

### src\services\code-index\shared\validation-helpers.ts
**Purpose:** Provides helper functions for error message sanitization and validation.

**Exported Functions:**
- `sanitizeErrorMessageerrorMessage: string` → `string`
- `getErrorMessageForStatusstatusCode: number` → `string`
- `extractStatusCodeerror: any` → `number | undefined`
- `extractErrorMessageerror: any` → `string | undefined`
- `handleValidationErrorerror: any` → `string`
- `formatEmbeddingErrorerror: any` → `string`
- `replaceinput: string, pattern: RegExp, replacement: string` → `string`

**Key Imports:** `"../../../i18n"`, `"serialize-error"`

---

### src\services\code-index\state-manager.ts
**Purpose:** Manages the state of the code indexing process.

**Exported Types:**
- `type IndexingState`: Standby, Indexing, Indexed, Error
- `class CodeIndexStateManager`: _systemStatus: IndexingState, _statusMessage: string, _processedItems: number, _totalItems: number

**Key Imports:** `"vscode"`

---

### src\services\code-index\vector-store\__tests__\qdrant-client.spec.ts
**Purpose:** Tests the QdrantVectorStore class for vector database interactions.

**Key Imports:** `@qdrant/js-client-rest`, `crypto`, `../qdrant-client`, `../../../../utils/path`, `../../constants`

---

### src\services\code-index\vector-store\qdrant-client.ts
**Purpose:** Implements the IVectorStore interface using a Qdrant vector database.

**Exported Functions:**
- `constructor(workspacePath: string, url: string, vectorSize: number, apiKey?: string)` → `void`

**Exported Types:**
- `class QdrantVectorStore`: vectorSize: number, DISTANCE_METRIC: string, client: QdrantClient, collectionName: string, qdrantUrl: string
- `interface IVectorStore`: addVectors, search, deleteVectors, updateVectors, getVectors
- `type Payload`: string: any
- `type VectorStoreSearchResult`: vectorId: string, score: number, payload: Payload | undefined

**Key Imports:** `@qdrant/js-client-rest`, `crypto`, `path`, `../../../utils/path`, `../interfaces/vector-store`

---

### src\services\command\__tests__\built-in-commands.spec.ts
**Purpose:** Tests the built-in commands retrieval and content verification.

**Key Imports:** `../built-in-commands`

---

### src\services\command\__tests__\frontmatter-commands.spec.ts
**Purpose:** Tests command loading with frontmatter for descriptions and metadata.

**Key Imports:** `fs`, `path`, `../commands`

---

### src\services\command\built-in-commands.ts
**Purpose:** Defines and retrieves built-in commands for code analysis and generation.

**Exported Functions:**
- `getBuiltInCommands()` → `Promise<BuiltInCommandDefinition[]>`
- `getBuiltInCommand(name: string)` → `Promise<Command | undefined>`
- `getBuiltInCommandNames()` → `Promise<string[]>`

**Exported Types:**
- `interface BuiltInCommandDefinition`: name: string, description: string, argumentHint?: string, content: string

**Exported Constants:**
- `BUILT_IN_COMMANDS` = `Record<string, BuiltInCommandDefinition>`

**Key Imports:** `../command/commands`, `fs`

---

### src\services\command\commands.ts
**Purpose:** Manages and retrieves commands from various sources, including built-in ones.

**Exported Functions:**
- `getCommands(cwd: string)` → `Promise<Command[]>`
- `getCommand(cwd: string, commandName: string)` → `Promise<Command | undefined>`
- `tryLoadCommand(filePath: string)` → `Promise<Command | undefined>`
- `getCommandNames(cwd: string)` → `Promise<string[]>`
- `scanCommandDirectory(dirPath: string, source: "global" | "project", commands: Map<string, Command>)` → `Promise<void>`
- `getCommandNameFromFile(filePath: string)` → `string | undefined`
- `isMarkdownFile(filePath: string)` → `boolean`

**Exported Types:**
- `interface Command`: name: string, content: string, source: "global" | "project" | "built-in", filePath: string, description?: string

**Key Imports:** `fs`, `path`, `gray-matter`, `../roo-config`, `./built-in-commands`

---

### src\services\glob\__mocks__\list-files.ts
**Purpose:** Provides a mock implementation for the listFiles function for testing.

**Exported Functions:**
- `listFiles(dirPath: string, _recursive: boolean, limit: number)` → `Promise<[string[], boolean]>`

---

### src\services\glob\__tests__\gitignore-integration.spec.ts
**Purpose:** Tests gitignore integration within the list-files functionality.

**Key Imports:** `path`, `fs`, `os`, `../list-files`, `child_process`

---

### src\services\glob\__tests__\gitignore-test.spec.ts
**Purpose:** Tests gitignore support for listing files in recursive mode.

**Key Imports:** `path`, `fs`, `os`, `../list-files`, `child_process`

---

### src\services\glob\__tests__\list-files-limit.spec.ts
**Purpose:** Verifies listFiles prevents stack overflow in large projects.

**Key Imports:** `path`, `fs`, `../list-files`, `child_process`

---

### src\services\glob\__tests__\list-files.spec.ts
**Purpose:** Tests the listFiles function's symlink and limit behaviors.

**Key Imports:** `path`, `childProcess`, `../list-files`, `fs`

---

### src\services\glob\constants.ts
**Purpose:** Defines a list of directories to ignore during file system operations.

**Exported Constants:**
- `DIRS_TO_IGNORE` = `["node_modules", "__pycache__", "env", "venv", "target/dependency", "build/dependencies", "dist", "out", "bundle", "vendor", "tmp", "temp", "deps", "pkg", "Pods", ".git", ".*"]`

---

### src\services\glob\ignore-utils.ts
**Purpose:** Provides utility functions for checking if a path is ignored.

**Exported Functions:**
- `isPathInIgnoredDirectory(filePath: string)` → `boolean`

**Key Imports:** `./constants`

---

### src\services\glob\list-files.ts
**Purpose:** Lists files in a directory, handling recursion and gitignore patterns.

**Exported Functions:**
- `listFiles(dirPath: string, recursive: boolean, limit: number)` → `Promise<[string[], boolean]>`
- `getFirstLevelDirectories(dirPath: string)` → `Promise<string[]>`
- `ensureFirstLevelDirectoriesIncluded(dirPath: string, directories: string[])` → `Promise<string[]>`
- `handleSpecialDirectories(dirPath: string)` → `Promise<[string[], boolean] | undefined>`
- `getRipgrepPath()` → `Promise<string>`
- `listFilesWithRipgrep(dirPath: string, recursive: boolean, limit: number, ignoreInstance: ReturnType<typeof ignore>)` → `Promise<[string[], boolean]>`
- `buildRipgrepArgs(dirPath: string, recursive: boolean, ignoreInstance: ReturnType<typeof ignore>)` → `string[]`
- `buildRecursiveArgs()` → `string[]`
- `buildNonRecursiveArgs()` → `string[]`
- `createIgnoreInstance(dirPath: string)` → `Promise<ReturnType<typeof ignore>>`
- `findGitignoreFiles(dirPath: string)` → `Promise<string[]>`
- `listFilteredDirectories(dirPath: string, recursive: boolean, ignoreInstance: ReturnType<typeof ignore>)` → `Promise<string[]>`
- `scanDirectory(dirPath: string, recursive: boolean, ignoreInstance: ReturnType<typeof ignore>, limit: number, results: string[])` → `Promise<[string[], boolean]>`
- `matchesIgnorePattern(filePath: string, ignoreInstance: ReturnType<typeof ignore>)` → `boolean`
- `isIgnoredByGitignore(filePath: string, ignoreInstance: ReturnType<typeof ignore>)` → `boolean`
- `shouldIncludeTargetDirectory(context: ScanContext)` → `boolean`
- `shouldIncludeInsideHiddenTarget(context: ScanContext)` → `boolean`
- `shouldIncludeRegularDirectory(context: ScanContext)` → `boolean`
- `shouldIncludeDirectory(context: ScanContext)` → `boolean`
- `isDirectoryExplicitlyIgnored(dirPath: string)` → `boolean`
- `formatAndCombineResults(results: string[], limit: number)` → `[string[], boolean]`
- `execRipgrep(args: string[], cwd: string)` → `Promise<string>`
- `processRipgrepOutput(output: string, limit: number)` → `[string[], boolean]`

**Exported Types:**
- `interface ScanContext`: isTargetDir: boolean, insideExplicitHiddenTarget: boolean, basePath: string, ignoreInstance: ReturnType<typeof ignore>

**Key Imports:** `os`, `path`, `fs`, `child_process`, `vscode`, `ignore`, `../../utils/path`, `../../services/ripgrep`, `./constants`

---

### src\services\marketplace\__tests__\marketplace-setting-check.spec.ts
**Purpose:** Tests marketplace API calls and installations with general availability.

**Key Imports:** `../../../core/webview/webviewMessageHandler`

---

### src\services\marketplace\__tests__\MarketplaceManager.spec.ts
**Purpose:** Tests the MarketplaceManager's functionality.

**Key Imports:** `@roo-code/types`, `../MarketplaceManager`

---

### src\services\marketplace\__tests__\nested-parameters.spec.ts
**Purpose:** Tests nested parameter validation within MCP installation methods.

**Key Imports:** `@roo-code/types`

---

### src\services\marketplace\__tests__\optional-parameters.spec.ts
**Purpose:** Tests optional parameter validation for MCP items.

**Key Imports:** `@roo-code/types`

---

### src\services\marketplace\__tests__\RemoteConfigLoader.spec.ts
**Purpose:** Tests the RemoteConfigLoader's ability to fetch marketplace items.

**Key Imports:** `axios`, `../RemoteConfigLoader`, `@roo-code/types`

---

### src\services\marketplace\__tests__\SimpleInstaller.spec.ts
**Purpose:** Tests the SimpleInstaller's installation of marketplace items.

**Key Imports:** `../SimpleInstaller`, `fs/promises`, `yaml`, `vscode`

---

### src\services\marketplace\index.ts
**Purpose:** Exports marketplace-related types and managers.

**Exported Types:**
- `type MarketplaceItemType`

---

### src\services\marketplace\MarketplaceManager.ts
**Purpose:** Manages fetching and installing marketplace items.

**Exported Types:**
- `interface MarketplaceItemsResponse`: organizationMcps, marketplaceItems, errors?

**Key Imports:** `fs/promises`, `path`, `vscode`, `yaml`, `@roo-code/types`

---

### src\services\marketplace\RemoteConfigLoader.ts
**Purpose:** Loads marketplace configuration from remote sources.

**Key Imports:** `axios`, `yaml`, `zod`, `@roo-code/types`, `@roo-code/cloud`

---

### src\services\marketplace\SimpleInstaller.ts
**Purpose:** Installs marketplace items, handling different types.

**Exported Types:**
- `interface InstallOptions`: target, selectedIndex?

**Key Imports:** `vscode`, `path`, `fs/promises`, `yaml`, `@roo-code/types`

---

### src\services\mcp\__tests__\McpHub.spec.ts
**Purpose:** Tests the McpHub service, mocking dependencies for isolated testing.

**Key Imports:** `fs`, `vitest`, `vscode`, `ClineProvider`, `McpHub`

---

### src\services\mcp\McpHub.ts
**Purpose:** Manages MCP server connections and resource interactions.

**Exported Types:**
- `type ConnectedMcpConnection`: type, server, client, transport

**Key Imports:** `@modelcontextprotocol/sdk/client/index.js`, `@modelcontextprotocol/sdk/client/stdio.js`, `@modelcontextprotocol/sdk/client/sse.js`, `@modelcontextprotocol/sdk/client/streamableHttp.js`, `reconnecting-eventsource`

---

### src\services\mcp\McpServerManager.ts
**Purpose:** Manages the singleton instance of McpHub.

**Key Imports:** `vscode`, `./McpHub`, `../../core/webview/ClineProvider`

---

### src\services\mdm\__tests__\MdmService.spec.ts
**Purpose:** Tests the MdmService class, mocking dependencies for behavior verification.

**Key Imports:** `path`, `fs`, `os`, `vscode`, `MdmService`, `CloudService`

---

### src\services\mdm\MdmService.ts
**Purpose:** Manages MDM configuration and cloud authentication requirements.

**Exported Types:**
- `type MdmConfig`: requireCloudAuth, organizationId
- `type ComplianceResult`: compliant, reason
- `class MdmService`: initialize, requiresCloudAuth

**Key Imports:** `fs`, `path`, `os`, `zod`, `CloudService`, `t`

---

### src\services\ripgrep\__tests__\index.spec.ts
**Purpose:** Tests the ripgrep line truncation function for various scenarios.

**Key Imports:** `truncateLine`

---

### src\services\ripgrep\index.ts
**Purpose:** Provides ripgrep integration for regex-based file searching functionality.

**Exported Functions:**
- `processDataany` → `any`
- `truncateLinestring` → `string`
- `getBinPath` → `Promise<string | undefined>`
- `execRipgrepstring[], workspacePath: string, limit?: number` → `Promise<childProcess.SpawnSyncReturns<string>>`
- `regexSearchFilescwd: string, directoryPath: string, regex: string, filePattern?: string` → `Promise<string>`
- `formatResultsstring, string, string, number` → `string`
- `checkPathstring` → `Promise<boolean>`

**Key Imports:** `childProcess`, `path`, `readline`, `vscode`, `RooIgnoreController`, `fileExistsAtPath`

---

### src\services\roo-config\__tests__\index.spec.ts
**Purpose:** Tests Roo configuration service functions for directory and file operations.

**Key Imports:** `path`, `getGlobalRooDirectory`, `getProjectRooDirectoryForCwd`, `directoryExists`, `fileExists`, `readFileIfExists`, `getRooDirectoriesForCwd`, `loadConfiguration`

---

### src\services\roo-config\index.ts
**Purpose:** Manages Roo configuration directories and configuration loading.

**Exported Functions:**
- `getGlobalRooDirectory` → `string`
- `getProjectRooDirectoryForCwdcwd: string` → `string`
- `directoryExistsdirPath: string` → `Promise<boolean>`
- `fileExistsfilePath: string` → `Promise<boolean>`
- `readFileIfExistsfilePath: string` → `Promise<string | undefined>`
- `getRooDirectoriesForCwdcwd: string` → `Promise<string[]>`
- `loadConfigurationcwd: string` → `Promise<any>`

**Key Imports:** `path`, `os`, `fs`

---

### src\services\search\file-search.ts
**Purpose:** Provides file search functionality using ripgrep and fuzzy search.

**Exported Types:**
- `type FileResult`: path, type, label

**Key Imports:** `vscode`, `path`, `fs`, `childProcess`, `readline`, `byLengthAsc`, `Fzf`, `getBinPath`

---

### src\services\tree-sitter\__tests__\fixtures\sample-c-sharp.ts
**Purpose:** Demonstrates C# code structures for tree-sitter parsing tests.

**Exported Functions:**
- `TestInterfaceMethodstring` → `void`
- `TestInterfaceCalculateMethodint, int` → `int`
- `ToString` → `string`
- `new` → `any`

**Exported Types:**
- `class TestAttributeDefinition`: Category, Priority
- `interface ITestInterfaceDefinition`: TestInterfaceMethod, TestInterfaceFormatMethod, TestInterfaceCalculateMethod
- `enum TestEnumDefinition`: Debug, Info, Warning, Error, Critical
- `class TestClassDefinition`: _prefix, _instanceCount

**Key Imports:** `System`, `System.Collections.Generic`, `System.Linq`, `System.Threading.Tasks`

---

### src\services\tree-sitter\__tests__\fixtures\sample-c.ts
**Purpose:** Provides C code examples for tree-sitter parsing tests.

**Exported Constants:**
- `MAX_SIZE` = `1024`
- `BUFFER_SIZE` = `MAX_SIZE * 2`
- `TIMEOUT_MS` = `1000 * 60 * 5`

---

### src\services\tree-sitter\__tests__\fixtures\sample-cpp.ts
**Purpose:** Demonstrates C++ code structures for tree-sitter parsing tests.

**Exported Functions:**
- `multiline_function_prototypeint, const std::string&, double, bool*` → `void`
- `function_with_implementationint, bool` → `void`

**Exported Types:**
- `type four_field_struct`: field1, field2, field3, field4
- `class base_class_definition`: virtual_method, protected_member
- `type four_member_union`: integer_value, float_value, char_value, double_value
- `enum scoped_enumeration`: Value1, Value2, Value3, Value4
- `type complex_type_definition`

---

### src\services\tree-sitter\__tests__\fixtures\sample-css.ts
**Purpose:** Provides CSS examples for tree-sitter parsing tests.

---

### src\services\tree-sitter\__tests__\fixtures\sample-elisp.ts
**Purpose:** Demonstrates Elisp code structures for tree-sitter parsing tests.

---

### src\services\tree-sitter\__tests__\fixtures\sample-elixir.ts
**Purpose:** Provides Elixir code examples for tree-sitter parsing tests.

---

### src\services\tree-sitter\__tests__\fixtures\sample-embedded_template.ts
**Purpose:** Demonstrates embedded template code structures for parsing tests.

---

### src\services\tree-sitter\__tests__\fixtures\sample-go.ts
**Purpose:** Provides Go code examples for tree-sitter parsing tests.

**Exported Functions:**
- `TestFunctionDefinitionstring, int, bool` → `error`

**Exported Types:**
- `interface TestInterfaceDefinition`: TestInterfaceMethod1, TestInterfaceMethod2
- `type TestStructDefinition`: TestField1, TestField2, TestField3, testField4
- `type TestTypeDefinition`: Mutex, data, ch, done

**Exported Constants:**
- `TestConstDefinition1` = `"test1"`
- `TestConstDefinition2` = `"test2"`
- `TestConstDefinition3` = `"test3"`
- `TestConstDefinition4` = `42`

**Key Imports:** `fmt`, `sync`, `time`

---

### src\services\tree-sitter\__tests__\fixtures\sample-html.ts
**Purpose:** Demonstrates HTML structure with various elements and attributes.

**Exported Functions:**
- `testFunction` → ``

---

### src\services\tree-sitter\__tests__\fixtures\sample-java.ts
**Purpose:** Illustrates Java syntax including interfaces, enums, and classes.

**Exported Functions:**
- `testInterfaceDefaultMethodString input, T data` → `String`
- `formatMessageString message, Object... args` → `String`

**Exported Types:**
- `interface TestInterfaceDefinition`: testInterfaceMethod(String message, T data), testInterfaceDefaultMethod(String input, T data)
- `enum TestEnumDefinition`: DEBUG(0, "Debug Level"), INFO(1, "Info Level"), WARNING(2, "Warning Level"), ERROR(3, "Error Level")
- `class TestClassDefinition`: String message, T data
- `class TestAbstractClassDefinition`: abstractMethod(), concreteMethod()
- `class TestInnerClassDefinition`: innerMethod()
- `class TestStaticNestedClassDefinition`: staticNestedMethod()
- `class TestRecordDefinition`: String message, T data

**Key Imports:** `java.util.List`, `java.util.Map`, `java.util.function.Function`, `java.time.LocalDateTime`

---

### src\services\tree-sitter\__tests__\fixtures\sample-javascript.ts
**Purpose:** Demonstrates JavaScript syntax including functions and classes.

**Exported Functions:**
- `testFunctionDefinitionparam1, param2, param3` → ``
- `testAsyncFunctionDefinitionurl, options, timeout` → ``
- `testGeneratorFunctionDefinitionstart, end, step` → ``
- `testArrowFunctionDefinitionparam1, param2, callback` → ``
- `testMethodDefinitionparam1, param2` → ``
- `testStaticMethodDefinitionparam1, param2` → ``
- `testGetterDefinition` → ``
- `testSetterDefinitionvalue` → ``
- `testDecoratedMethodDefinitionparam1, param2` → ``

**Exported Types:**
- `class TestClassDefinition`: #privateField, static staticField, constructor(name, value), testMethodDefinition(param1, param2)

**Key Imports:** `react`, `react-dom`, `./utils`

---

### src\services\tree-sitter\__tests__\fixtures\sample-json.ts
**Purpose:** Provides examples of JSON structures with various data types.

---

### src\services\tree-sitter\__tests__\fixtures\sample-kotlin.ts
**Purpose:** Illustrates Kotlin syntax including classes, interfaces, and enums.

**Exported Functions:**
- `concreteMethodDefinitionString param1, Int param2` → `Int`
- `requiredMethodDefinitionString param1, Int param2` → `Boolean`
- `defaultMethodDefinitionString message` → `String`
- `updateStateFlowDefinition` → ``

**Exported Types:**
- `class TestAbstractClassDefinition`: abstractPropertyDefinition, abstractMethodDefinition(), concreteMethodDefinition(param1: String, param2: Int)
- `interface TestInterfaceDefinition`: interfacePropertyDefinition, requiredMethodDefinition(param1: String, param2: Int), defaultMethodDefinition(message: String)
- `enum TestEnumClassDefinition`: enumValue, enumDescription
- `class TestOuterClassDefinition`: TestInnerClassDefinition
- `class TestInnerClassDefinition`: innerMethod()
- `class TestNestedClassDefinition`: nestedMethod()
- `class TestSealedClassDefinition`: sealedMethod()

**Key Imports:** `kotlinx.coroutines.*`, `kotlinx.coroutines.flow.*`, `kotlin.math.sqrt`, `kotlin.properties.Delegates`

---

### src\services\tree-sitter\__tests__\fixtures\sample-lua.ts
**Purpose:** Demonstrates Lua syntax with functions and table structures.

**Exported Functions:**
- `test_functionarg1, arg2, arg3` → ``
- `test_local_functionparam1, param2, param3` → ``

---

### src\services\tree-sitter\__tests__\fixtures\sample-ocaml.ts
**Purpose:** Shows OCaml syntax with modules, types, and functions.

---

### src\services\tree-sitter\__tests__\fixtures\sample-php.ts
**Purpose:** Illustrates PHP syntax including classes, traits, and interfaces.

**Exported Functions:**
- `standardInterfaceMethodWithClassstring $value` → `void`
- `standardInterfaceMethodNullable?string $value` → `void`
- `standardInterfaceMethodVoid` → `void`
- `standardInterfaceMethodMixedstring|int $value` → `string|int`
- `standardTraitMethodstring $value` → `string`
- `standardTraitAbstractMethodstring $value` → `string`
- `standardEnumMethodStandardEnumDefinition $enum` → `string`
- `standardEnumFromStringstring $value` → `StandardEnumDefinition`
- `standardAbstractMethodstring $value` → `string`
- `standardStaticMethodstring $value` → `string`
- `validateConfigarray $config` → `bool`
- `standardUnionTypesMethodstring|int $value` → `string|int`
- `standardIntersectionTypesMethodStandardInterfaceDefinition&AnotherInterfaceDefinition $value` → `void`
- `standardAnonymousMethodstring $value` → `string`
- `standardGlobalFunctionstring $value` → `string`
- `matchstring $value` → `string`

**Exported Types:**
- `class StandardAttributeDefinition`: private string $description, private int $priority, private array $tags
- `class StandardClassDefinition`: private string $standardProperty, public function standardMethod(): string

**Key Imports:** `StandardNamespaceDefinition\Interfaces\StandardInterfaceDefinition`, `StandardNamespaceDefinition\Interfaces\AnotherInterfaceDefinition`, `StandardNamespaceDefinition\Traits\StandardTraitDefinition`, `StandardNamespaceDefinition\Traits\LoggableTraitDefinition`, `StandardNamespaceDefinition\Enums\StandardEnumDefinition`

---

### src\services\tree-sitter\__tests__\fixtures\sample-python.ts
**Purpose:** Demonstrates Python syntax with classes, functions, and decorators.

---

### src\services\tree-sitter\__tests__\fixtures\sample-ruby.ts
**Purpose:** Shows Ruby syntax with classes and method definitions.

---

### src\services\tree-sitter\__tests__\fixtures\sample-rust.ts
**Purpose:** Demonstrates Rust syntax including functions and structs.

**Exported Functions:**
- `test_function_definitioni32 param1, &str param2, Option<String> param3, Vec<u8> param4` → `Result<i32, String>`
- `test_async_function_definition&str url, std::time::Duration timeout, u32 retry_count, Vec<(&str, &str)> headers` → `Result<String, Box<dyn std::error::Error>>`
- `test_const_function_definitionT value, usize multiplier, &'static str prefix, &'static str suffix` → `[T; 4]`
- `is_nullOption<T> opt` → `bool`

**Exported Types:**
- `class test_struct_definition`: name: String, value: i32, data: Option<Vec<f64>>, metadata: std::collections::HashMap<String, i32>
- `class test_tuple_struct_definition`: String, i32, Option<Vec<f64>>, std::collections::HashMap<String, i32>

---

### src\services\tree-sitter\__tests__\fixtures\sample-scala.ts
**Purpose:** Illustrates Scala syntax including classes, traits, and objects.

**Exported Functions:**
- `RichStringval str: String` → ``

**Exported Types:**
- `class Container`: first: A, second: B, swap
- `class TestCaseClass`: field1: A, field2: B, field3: List[A]
- `class AbstractBase`: abstractMethod, abstractValue
- `interface TestTrait`: type T, method
- `class SingletonValue`: abstractMethod, abstractValue

**Key Imports:** `scala.collection.mutable`, `scala.concurrent.Future`

---

### src\services\tree-sitter\__tests__\fixtures\sample-solidity.ts
**Purpose:** Demonstrates Solidity syntax with interfaces, libraries, and contracts.

**Exported Functions:**
- `interfaceFunctionuint256 value` → `bool`
- `adduint256 a, uint256 b` → `uint256`
- `subtractuint256 a, uint256 b` → `uint256`
- `transferaddress to, uint256 amount` → ``
- `returns` → `uint256`
- `onlyAdmin` → ``
- `constructoruint256 _totalSupply` → ``

**Exported Types:**
- `interface ITestInterface`: interfaceFunction(uint256 value), event InterfaceEvent(address indexed sender, uint256 value), error InterfaceError(string message)
- `class UserInfo`: address userAddress, uint256 balance, mapping(bytes32 => bool) permissions, uint256 lastUpdate
- `enum UserRole`: None, Basic, Admin, SuperAdmin

---

### src\services\tree-sitter\__tests__\fixtures\sample-swift.ts
**Purpose:** Illustrates Swift syntax including classes, structs, and methods.

**Exported Functions:**
- `modifyingMethod` → ``

**Exported Types:**
- `class StandardClassDefinition`: private var standardProperty, standardMethod()
- `class FinalClassDefinition`: private let finalProperty, finalClassMethod(parameter: String)
- `class OpenClassDefinition`: public var openProperty, openOverridableMethod(parameter1: String, parameter2: Int)
- `class InheritingClassDefinition`: protocolRequiredProperty, override standardMethod(), protocolRequiredMethod(with parameter: String)
- `class StandardStructDefinition`: private var standardStructProperty, let readOnlyProperty, mutating func modifyingMethod()

---

### src\services\tree-sitter\__tests__\fixtures\sample-systemrdl.ts
**Purpose:** This file provides SystemRDL examples for tree-sitter parsing tests.

---

### src\services\tree-sitter\__tests__\fixtures\sample-tlaplus.ts
**Purpose:** This file contains TLA+ module examples for tree-sitter testing.

---

### src\services\tree-sitter\__tests__\fixtures\sample-toml.ts
**Purpose:** It provides TOML examples for tree-sitter parsing tests.

**Exported Constants:**
- `sampleToml` = ``# This is a TOML document with various structures...``

---

### src\services\tree-sitter\__tests__\fixtures\sample-tsx.ts
**Purpose:** This file provides TSX examples for tree-sitter parsing tests.

**Exported Types:**
- `interface StandardInterfaceProps`: required: string, numeric: number, callback: () => void, complex: { id: string; value: number }[]
- `type StandardTypeAlias`: id: string, name: string, timestamp: Date, status: 'active' | 'inactive'
- `interface PropsDefinitionExample`: requiredString: string, requiredNumber: number, requiredCallback: (value: string) => void, optionalBoolean?: boolean, optionalObject?: { key: string }, optionalArray?: string[]

---

### src\services\tree-sitter\__tests__\fixtures\sample-typescript.ts
**Purpose:** This file provides TypeScript examples for tree-sitter parsing tests.

**Exported Types:**
- `interface TestInterfaceDefinition`: name: string, value: number, methodSignature(param1: string, param2: number): string
- `type TestTypeDefinition`: id: number, name: string, callback: (param: string) => void
- `enum TestEnumDefinition`: First = 'FIRST', Second = 'SECOND', Third = 'THIRD', Fourth = 'FOURTH'
- `interface InnerInterface`: prop: string
- `interface TestGenericInterfaceDefinition`: data: T, metadata: U, process(input: T): U

**Key Imports:** `react`, `react-dom`, `./utils`

---

### src\services\tree-sitter\__tests__\fixtures\sample-vue.ts
**Purpose:** This file provides Vue examples for tree-sitter parsing tests.

**Exported Constants:**
- `sampleVue` = ``
<template>...
</template>
``

---

### src\services\tree-sitter\__tests__\fixtures\sample-zig.ts
**Purpose:** This file provides Zig examples for tree-sitter parsing tests.

**Exported Types:**
- `class Point`: x: f32, y: f32, init(x: f32, y: f32) Point, distance(self: Point) f32
- `enum Direction`: North, South, East, West
- `class Vector`: direction: Direction, magnitude: f32

**Exported Constants:**
- `VERSION` = `1`

---

### src\services\tree-sitter\__tests__\helpers.ts
**Purpose:** It provides helper functions for tree-sitter testing and initialization.

**Exported Functions:**
- `initializeTreeSitter` → `Promise<void>`
- `debugLogmessage: string, ...args: any[]` → `void`

**Key Imports:** `../index`, `fs/promises`, `path`, `web-tree-sitter`

---

### src\services\tree-sitter\__tests__\index.spec.ts
**Purpose:** This file tests the tree-sitter service's core functionality.

**Key Imports:** `fs/promises`, `vitest`, `../index`, `../../glob/list-files`, `../languageParser`, `../../../utils/fs`

---

### src\services\tree-sitter\__tests__\inspectC.spec.ts
**Purpose:** This file tests C code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-c`

---

### src\services\tree-sitter\__tests__\inspectCpp.spec.ts
**Purpose:** This file tests C++ code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-cpp`

---

### src\services\tree-sitter\__tests__\inspectCSharp.spec.ts
**Purpose:** This file tests C# code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-c-sharp`

---

### src\services\tree-sitter\__tests__\inspectCSS.spec.ts
**Purpose:** This file tests CSS code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-css`

---

### src\services\tree-sitter\__tests__\inspectElisp.spec.ts
**Purpose:** This file tests Elisp code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries/elisp`, `./fixtures/sample-elisp`

---

### src\services\tree-sitter\__tests__\inspectElixir.spec.ts
**Purpose:** This file tests Elixir code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-elixir`

---

### src\services\tree-sitter\__tests__\inspectEmbeddedTemplate.spec.ts
**Purpose:** This file tests embedded template code inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-embedded_template`

---

### src\services\tree-sitter\__tests__\inspectGo.spec.ts
**Purpose:** This file tests Go code structure inspection and parsing.

**Key Imports:** `./helpers`, `./fixtures/sample-go`, `../queries/go`

---

### src\services\tree-sitter\__tests__\inspectHtml.spec.ts
**Purpose:** This file tests HTML code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-html`

---

### src\services\tree-sitter\__tests__\inspectJava.spec.ts
**Purpose:** This file tests Java code structure inspection and parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-java`

---

### src\services\tree-sitter\__tests__\inspectJavaScript.spec.ts
**Purpose:** Tests JavaScript tree structure inspection and definition parsing.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-javascript`

---

### src\services\tree-sitter\__tests__\inspectJson.spec.ts
**Purpose:** Tests JSON tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-json`

---

### src\services\tree-sitter\__tests__\inspectKotlin.spec.ts
**Purpose:** Tests Kotlin tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-kotlin`

---

### src\services\tree-sitter\__tests__\inspectLua.spec.ts
**Purpose:** Tests Lua tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-lua`

---

### src\services\tree-sitter\__tests__\inspectOCaml.spec.ts
**Purpose:** Tests OCaml tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-ocaml`

---

### src\services\tree-sitter\__tests__\inspectPhp.spec.ts
**Purpose:** Tests PHP tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-php`

---

### src\services\tree-sitter\__tests__\inspectPython.spec.ts
**Purpose:** Tests Python tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `./fixtures/sample-python`, `../queries`

---

### src\services\tree-sitter\__tests__\inspectRuby.spec.ts
**Purpose:** Tests Ruby tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-ruby`

---

### src\services\tree-sitter\__tests__\inspectRust.spec.ts
**Purpose:** Tests Rust tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-rust`

---

### src\services\tree-sitter\__tests__\inspectScala.spec.ts
**Purpose:** Tests Scala tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-scala`

---

### src\services\tree-sitter\__tests__\inspectSolidity.spec.ts
**Purpose:** Tests Solidity tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-solidity`

---

### src\services\tree-sitter\__tests__\inspectSwift.spec.ts
**Purpose:** Tests Swift tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-swift`

---

### src\services\tree-sitter\__tests__\inspectSystemRDL.spec.ts
**Purpose:** Tests SystemRDL tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries/systemrdl`, `./fixtures/sample-systemrdl`

---

### src\services\tree-sitter\__tests__\inspectTLAPlus.spec.ts
**Purpose:** Tests TLA+ tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-tlaplus`

---

### src\services\tree-sitter\__tests__\inspectTOML.spec.ts
**Purpose:** Tests TOML tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-toml`

---

### src\services\tree-sitter\__tests__\inspectTsx.spec.ts
**Purpose:** Tests TSX tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `./fixtures/sample-tsx`

---

### src\services\tree-sitter\__tests__\inspectTypeScript.spec.ts
**Purpose:** Tests TypeScript tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-typescript`

---

### src\services\tree-sitter\__tests__\inspectVue.spec.ts
**Purpose:** Tests Vue tree structure inspection and definition parsing.

**Key Imports:** `./helpers`, `../queries/vue`, `./fixtures/sample-vue`

---

### src\services\tree-sitter\__tests__\inspectZig.spec.ts
**Purpose:** Tests Zig tree structure inspection and definition parsing.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-zig`

---

### src\services\tree-sitter\__tests__\languageParser.spec.ts
**Purpose:** Tests loading language parsers for different file types.

**Key Imports:** `path`, `../languageParser`

---

### src\services\tree-sitter\__tests__\markdownIntegration.spec.ts
**Purpose:** Tests markdown file parsing and header extraction for definition listing.

**Key Imports:** `fs/promises`, `vitest`, `../index`

---

### src\services\tree-sitter\__tests__\markdownParser.spec.ts
**Purpose:** Tests markdown parsing for ATX and Setext headers and captures.

**Exported Functions:**
- `processCaptures` → ``

**Key Imports:** `../markdownParser`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.c-sharp.spec.ts
**Purpose:** Tests C# source code definition parsing using tree-sitter queries.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-c-sharp`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.c.spec.ts
**Purpose:** Tests C source code definition parsing using tree-sitter queries.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-c`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.cpp.spec.ts
**Purpose:** Tests C++ source code definition parsing using tree-sitter queries.

**Exported Functions:**
- `field2` → ``

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-cpp`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.css.spec.ts
**Purpose:** Tests CSS source code definition parsing using tree-sitter queries.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-css`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.elisp.spec.ts
**Purpose:** Tests Elisp source code definition parsing using tree-sitter queries.

**Key Imports:** `./helpers`, `../queries/elisp`, `./fixtures/sample-elisp`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.elixir.spec.ts
**Purpose:** Tests Elixir source code definition parsing using tree-sitter queries.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-elixir`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.embedded_template.spec.ts
**Purpose:** Tests embedded template parsing for source code definitions.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-embedded_template`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.go.spec.ts
**Purpose:** Tests Go source code definition parsing using tree-sitter queries.

**Key Imports:** `./fixtures/sample-go`, `./helpers`, `../queries/go`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.html.spec.ts
**Purpose:** Tests HTML source code definition parsing using tree-sitter queries.

**Key Imports:** `./fixtures/sample-html`, `../queries`, `./helpers`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.java.spec.ts
**Purpose:** Tests Java source code definition parsing using tree-sitter queries.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-java`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.javascript.spec.ts
**Purpose:** Tests JavaScript source code definition parsing using tree-sitter queries.

**Exported Functions:**
- `toMatch` → ``

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-javascript`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.json.spec.ts
**Purpose:** Tests JSON structure parsing using tree-sitter and JavaScript queries.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-json`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.kotlin.spec.ts
**Purpose:** Tests Kotlin source code definition parsing using tree-sitter queries.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-kotlin`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.lua.spec.ts
**Purpose:** Tests Lua source code definition parsing using tree-sitter.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-lua`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.ocaml.spec.ts
**Purpose:** Tests OCaml source code definition parsing with tree-sitter.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-ocaml`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.php.spec.ts
**Purpose:** Tests PHP source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-php`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.python.spec.ts
**Purpose:** Tests Python source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `./fixtures/sample-python`, `../queries`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.ruby.spec.ts
**Purpose:** Tests Ruby source code definition parsing using tree-sitter.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-ruby`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.rust.spec.ts
**Purpose:** Tests Rust source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `./fixtures/sample-rust`, `../queries`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.scala.spec.ts
**Purpose:** Tests Scala source code definition parsing using tree-sitter.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-scala`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.solidity.spec.ts
**Purpose:** Tests Solidity source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-solidity`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.swift.spec.ts
**Purpose:** Tests Swift source code definition parsing using tree-sitter.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-swift`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.systemrdl.spec.ts
**Purpose:** Tests SystemRDL source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `../queries/systemrdl`, `./fixtures/sample-systemrdl`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.tlaplus.spec.ts
**Purpose:** Tests TLA+ source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-tlaplus`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.toml.spec.ts
**Purpose:** Tests TOML source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-toml`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.tsx.spec.ts
**Purpose:** Tests TSX source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `./fixtures/sample-tsx`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.typescript.spec.ts
**Purpose:** Tests TypeScript source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-typescript`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.vue.spec.ts
**Purpose:** Tests Vue source code definition parsing using tree-sitter.

**Key Imports:** `./helpers`, `./fixtures/sample-vue`, `../queries/vue`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.zig.spec.ts
---

### src\services\tree-sitter\index.ts
**Purpose:** Provides tree-sitter based parsing for code definitions and components.

**Exported Functions:**
- `getMinComponentLines` → `number`
- `setMinComponentLinesvalue: number` → `void`
- `parseSourceCodeDefinitionsForFilefilePath: string, fileContent: string, language: string` → `Promise<any[]>`
- `parseSourceCodeForDefinitionsTopLevelfileContent: string, language: string` → `any[]`
- `separateFilesfiles: string[], ignoreController: RooIgnoreController` → `Promise<string[]>`
- `processCapturescaptures: QueryCapture[], fileContent: string` → `any[]`
- `parseFilefilePath: string, fileContent: string, language: string` → `Promise<any>`

**Exported Constants:**
- `DEFAULT_MIN_COMPONENT_LINES_VALUE` = `4`

**Key Imports:** `fs`, `path`, `listFiles`, `LanguageParser`, `fileExistsAtPath`, `parseMarkdown`, `RooIgnoreController`, `QueryCapture`

---

### src\services\tree-sitter\languageParser.ts
**Purpose:** Loads and manages tree-sitter language parsers for various languages.

**Exported Types:**
- `interface LanguageParser`: parser, query

**Key Imports:** `path`, `ParserT`, `LanguageT`, `QueryT`, `javascriptQuery`, `typescriptQuery`, `tsxQuery`, `pythonQuery`

---

### src\services\tree-sitter\markdownParser.ts
**Purpose:** Parses markdown files to extract headers and section line ranges.

**Exported Functions:**
- `parseMarkdowncontent: string` → `QueryCapture[]`
- `formatMarkdownCapturescaptures: QueryCapture[], fileContent: string` → `any[]`

**Key Imports:** `QueryCapture`

---

### src\services\tree-sitter\queries\c-sharp.ts
**Purpose:** Defines C# tree-sitter query patterns for code analysis.

---

### src\services\tree-sitter\queries\c.ts
**Purpose:** Defines C language constructs for tree-sitter parsing.

---

### src\services\tree-sitter\queries\cpp.ts
**Purpose:** Defines C++ language structures for tree-sitter parsing.

---

### src\services\tree-sitter\queries\css.ts
**Purpose:** Defines CSS Tree-Sitter query patterns for various language constructs.

---

### src\services\tree-sitter\queries\elisp.ts
**Purpose:** Provides Emacs Lisp query patterns for function and macro definitions.

**Exported Constants:**
- `elispQuery` = ```

---

### src\services\tree-sitter\queries\elixir.ts
**Purpose:** Specifies Elixir query patterns for module, function, and macro definitions.

---

### src\services\tree-sitter\queries\embedded_template.ts
**Purpose:** Defines query patterns for embedded template code and output blocks.

---

### src\services\tree-sitter\queries\go.ts
**Purpose:** Captures Go language constructs using Tree-Sitter query patterns.

---

### src\services\tree-sitter\queries\html.ts
**Purpose:** Defines HTML query patterns for document structure and element definitions.

---

### src\services\tree-sitter\queries\index.ts
**Purpose:** Exports all language query modules for tree-sitter integration.

**Key Imports:** `./solidity`, `./php`, `./vue`, `./typescript`, `./tsx`

---

### src\services\tree-sitter\queries\java.ts
**Purpose:** Provides Java query patterns for module, class, and method declarations.

---

### src\services\tree-sitter\queries\javascript.ts
**Purpose:** Defines JavaScript query patterns for class and function definitions.

---

### src\services\tree-sitter\queries\kotlin.ts
**Purpose:** Specifies Kotlin query patterns for class and function declarations.

---

### src\services\tree-sitter\queries\lua.ts
**Purpose:** Defines Lua query patterns for function and variable definitions.

---

### src\services\tree-sitter\queries\ocaml.ts
**Purpose:** Captures OCaml module, type, and function definitions using queries.

**Exported Constants:**
- `ocamlQuery` = ```

---

### src\services\tree-sitter\queries\php.ts
**Purpose:** Defines PHP query patterns for class, interface, and function definitions.

---

### src\services\tree-sitter\queries\python.ts
**Purpose:** Provides Python query patterns for class and function definitions.

---

### src\services\tree-sitter\queries\ruby.ts
**Purpose:** Defines Ruby query patterns for method and class definitions.

---

### src\services\tree-sitter\queries\rust.ts
**Purpose:** Defines Rust query patterns for function, struct, and enum definitions.

---

### src\services\tree-sitter\queries\scala.ts
**Purpose:** Defines Scala query patterns for classes, objects, and methods.

**Exported Constants:**
- `scalaQuery` = ```

---

### src\services\tree-sitter\queries\solidity.ts
**Purpose:** Defines Solidity syntax queries for tree-sitter parsing.

---

### src\services\tree-sitter\queries\swift.ts
**Purpose:** Provides Swift query patterns for tree-sitter language parsing.

---

### src\services\tree-sitter\queries\systemrdl.ts
**Purpose:** Captures SystemRDL structures using tree-sitter query patterns.

---

### src\services\tree-sitter\queries\tlaplus.ts
**Purpose:** Defines TLA+ structures for tree-sitter query pattern matching.

---

### src\services\tree-sitter\queries\toml.ts
**Purpose:** Provides TOML syntax element queries for tree-sitter parsing.

**Exported Constants:**
- `tomlQuery` = `string`

---

### src\services\tree-sitter\queries\tsx.ts
**Purpose:** Defines TSX queries for React component definitions in TSX files.

**Key Imports:** `./typescript`

---

### src\services\tree-sitter\queries\typescript.ts
**Purpose:** Defines TypeScript syntax queries for tree-sitter parsing.

---

### src\services\tree-sitter\queries\vue.ts
**Purpose:** Defines Vue syntax queries for tree-sitter parsing.

**Exported Constants:**
- `vueQuery` = `string`

---

### src\services\tree-sitter\queries\zig.ts
**Purpose:** Defines Zig syntax queries for tree-sitter parsing.

**Exported Constants:**
- `zigQuery` = `string`

---

### src\shared\__tests__\api.spec.ts
**Purpose:** Tests the retrieval of model max output tokens based on settings.

**Key Imports:** `import { type ModelInfo, type ProviderSettings, CLAUDE_CODE_DEFAULT_MAX_OUTPUT_TOKENS, ANTHROPIC_DEFAULT_MAX_TOKENS } from "@roo-code/types"`, `import { getModelMaxOutputTokens, shouldUseReasoningBudget, shouldUseReasoningEffort } from "../api"`

---

### src\shared\__tests__\checkExistApiConfig.spec.ts
**Purpose:** Tests the check for existing API configuration keys.

**Key Imports:** `import type { ProviderSettings } from "@roo-code/types"`, `import { checkExistKey } from "../checkExistApiConfig"`

---

### src\shared\__tests__\combineApiRequests.spec.ts
**Purpose:** Tests the combination of API request messages.

**Key Imports:** `import type { ClineMessage, ClineSay } from "@roo-code/types"`, `import { combineApiRequests } from "../combineApiRequests"`

---

### src\shared\__tests__\combineCommandSequences.spec.ts
**Purpose:** Tests the combination of command sequence messages.

**Key Imports:** `import type { ClineMessage } from "@roo-code/types"`, `import { combineCommandSequences } from "../combineCommandSequences"`

---

### src\shared\__tests__\context-mentions.spec.ts
**Purpose:** Tests regular expressions for identifying context mentions.

**Key Imports:** `import { mentionRegex, mentionRegexGlobal } from "../context-mentions"`

---

### src\shared\__tests__\experiments-preventFocusDisruption.spec.ts
**Purpose:** Tests the PREVENT_FOCUS_DISRUPTION experiment configuration and behavior.

**Key Imports:** `import { EXPERIMENT_IDS, experimentConfigsMap, experimentDefault, experiments } from "../experiments"`

---

### src\shared\__tests__\experiments.spec.ts
**Purpose:** Tests experiment configurations and their enabled states.

**Key Imports:** `import type { ExperimentId } from "@roo-code/types"`, `import { EXPERIMENT_IDS, experimentConfigsMap, experiments as Experiments } from "../experiments"`

---

### src\shared\__tests__\getApiMetrics.spec.ts
**Purpose:** Tests the calculation of API metrics from Cline messages.

**Key Imports:** `import type { ClineMessage } from "@roo-code/types"`, `import { getApiMetrics } from "../getApiMetrics"`

---

### src\shared\__tests__\language.spec.ts
**Purpose:** Tests the `formatLanguage` function for locale formatting.

**Exported Functions:**
- `formatLanguagestring` → `string`

**Key Imports:** `../language`

---

### src\shared\__tests__\modes-empty-prompt-component.spec.ts
**Purpose:** Tests `getModeSelection` with empty or null prompt components.

**Exported Types:**
- `interface PromptComponent`: roleDefinition, cus

**Key Imports:** `@roo-code/types`, `../modes`

---

### src\shared\__tests__\modes.spec.ts
**Purpose:** Tests tool allowance and mode selection based on configurations.

**Exported Functions:**
- `isToolAllowedForModestring, string, ModeConfig[]` → `boolean`
- `getFullModeDetailsstring, ModeConfig[]` → `any`
- `getModeSelectionstring, PromptComponent | undefined | null, any[]` → `any`

**Exported Types:**
- `type ModeConfig`: slug, name, roleDefinition, groups
- `interface PromptComponent`: roleDefinition, cus

**Key Imports:** `@roo-code/types`, `../modes`, `../../core/prompts/sections/custom-instructions`

---

### src\shared\__tests__\ProfileValidator.spec.ts
**Purpose:** Tests the `ProfileValidator` for allowing provider profiles.

**Exported Functions:**
- `isProfileAllowedProviderSettings, OrganizationAllowList` → `boolean`

**Exported Types:**
- `type ProviderSettings`: apiProvider, openAiModelId
- `type OrganizationAllowList`: allowAll, providers

**Key Imports:** `@roo-code/types`, `../ProfileValidator`

---

### src\shared\__tests__\support-prompts.spec.ts
**Purpose:** Tests the formatting of prompts for code actions.

**Exported Functions:**
- `createstring, { filePath: string; selectedText: string; diagnostics?: any[]; }` → `string`

**Key Imports:** `../support-prompt`

---

### src\shared\__tests__\vsCodeSelectorUtils.spec.ts
**Purpose:** Tests stringification of VS Code language model selectors.

**Exported Functions:**
- `stringifyVsCodeLmModelSelectorLanguageModelChatSelector` → `string`

**Exported Types:**
- `type LanguageModelChatSelector`: vendor, family, version, id

**Key Imports:** `vscode`, `../vsCodeSelectorUtils`

---

### src\shared\api.ts
**Purpose:** Defines API handler options, router names, and model records.

**Exported Types:**
- `type ApiHandlerOptions`: enableGpt5ReasoningSummary?: boolean, ollamaNumCtx?: number
- `type RouterName`
- `type ModelRecord`
- `type RouterModels`

**Key Imports:** `@roo-code/types`, `Omit`

---

### src\shared\array.ts
**Purpose:** Provides utility functions for finding elements in arrays.

**Exported Functions:**
- `findLastIndexarray: Array<T>, predicate: (value: T, index: number, obj: T[]) => boolean` → `number`
- `findLastarray: Array<T>, predicate: (value: T, index: number, obj: T[]) => boolean` → `T | undefined`

---

### src\shared\checkExistApiConfig.ts
**Purpose:** Checks if a provider configuration contains necessary API keys.

**Exported Functions:**
- `checkExistKeyconfig: ProviderSettings | undefined` → `boolean`

**Key Imports:** `@roo-code/types`

---

### src\shared\combineApiRequests.ts
**Purpose:** Combines API request start and finish messages into one.

**Exported Functions:**
- `combineApiRequestsmessages: ClineMessage[]` → `ClineMessage[]`

**Key Imports:** `@roo-code/types`

---

### src\shared\combineCommandSequences.ts
**Purpose:** Combines command and output messages into single ClineMessages.

**Exported Functions:**
- `combineCommandSequencesmessages: ClineMessage[]` → `ClineMessage[]`

**Exported Constants:**
- `COMMAND_OUTPUT_STRING` = `"Output:"`

**Key Imports:** `@roo-code/types`, `./safeJsonParse`

---

### src\shared\context-mentions.ts
**Purpose:** Defines regular expressions for identifying and formatting mentions.

**Exported Functions:**
- `formatGitSuggestion` → ``
- `unescapeSpaces` → ``

---

### src\shared\cost.ts
**Purpose:** Calculates API costs based on token usage and model information.

**Exported Functions:**
- `calculateApiCostAnthropicmodelInfo: ModelInfo, inputTokens: number, outputTokens: number, cacheCreationInputTokens?: number, cacheReadInputTokens?: number` → `number`
- `calculateApiCostOpenAImodelInfo: ModelInfo, inputTokens: number, outputTokens: number, cacheCreationInputTokens?: number, cacheReadInputTokens?: number` → `number`
- `parseApiPrice` → ``

**Key Imports:** `@roo-code/types`

---

### src\shared\embeddingModels.ts
**Purpose:** Defines embedding model profiles with dimensions and thresholds.

**Exported Types:**
- `type EmbedderProvider`
- `interface EmbeddingModelProfile`: dimension: number, scoreThreshold?: number, queryPrefix?: string
- `type EmbeddingModelProfiles`

---

### src\shared\experiments.ts
**Purpose:** Manages experiment configurations and feature toggles.

**Exported Types:**
- `type ExperimentKey`
- `interface ExperimentConfig`: enabled: boolean

**Exported Constants:**
- `EXPERIMENT_IDS` = `{ MULTI_FILE_APPLY_DIFF: "multiFileApplyDiff", POWER_STEERING: "powerSteering", PREVENT_FOCUS_DISRUPTION: "preventFocusDisruption", IMAGE_GENERATION: "imageGeneration", RUN_SLASH_COMMAND: "runSlashCommand" }`
- `experimentDefault` = `Object.fromEntries( Object.entries(experimentConfigsMap).map(([_, config]) => [ EXPERIMENT_IDS[_ as keyof typeof EXPERIMENT_IDS] as ExperimentId, config.enabled, ]),)`

**Key Imports:** `@roo-code/types`

---

### src\shared\ExtensionMessage.ts
**Purpose:** Defines interfaces for communication between extension and webview.

**Exported Types:**
- `interface Command`: name: string, source: "global" | "project" | "built-in", filePath?: string
- `interface MarketplaceInstalledMetadata`: project: Record<string, { type: string }>, global: Record<string, { type: string }>
- `interface IndexingStatus`: systemStatus: string, message?: string, processedItems: number
- `interface IndexingStatusUpdateMessage`: type: "indexingStatusUpdate", values: IndexingStatus
- `interface LanguageModelChatSelector`: vendor?: string, family?: string, version?: string

**Key Imports:** `@roo-code/types`, `../utils/git`, `./mcp`, `./modes`, `./api`

---

### src\shared\getApiMetrics.ts
**Purpose:** Calculates API metrics from ClineMessages, including token usage.

**Exported Functions:**
- `getApiMetricsmessages: ClineMessage[]` → `{ totalTokensIn: number; totalTokensOut: number; totalCacheWrites: number | undefined; totalCacheReads: number | undefined; totalCost: number; contextTokens: number; }`
- `hasTokenUsageChanged` → ``

**Exported Types:**
- `type ParsedApiReqStartedTextType`: tokensIn: number, tokensOut: number, cacheWrites: number, cacheReads: number

**Key Imports:** `@roo-code/types`

---

### src\shared\globalFileNames.ts
**Purpose:** Defines global file names used within the application.

**Exported Constants:**
- `GlobalFileNames` = `{ apiConversationHistory: "api_conversation_history.json", uiMessages: "ui_messages.json", mcpSettings: "mcp_settings.json", customModes: "custom_modes.yaml", taskMetadata: "task_metadata.json" }`

---

### src\shared\language.ts
**Purpose:** Provides language formatting and mapping functionalities.

**Exported Functions:**
- `formatLanguagevscodeLocale: string` → `Language`

**Exported Constants:**
- `LANGUAGES` = `{ ca: "Català", de: "Deutsch", en: "English", es: "Español", fr: "Français", hi: "हिन्दी", id: "Bahasa Indonesia", it: "Italiano", ja: "日本語", ko: "한국어", nl: "Nederlands", pl: "Polski", "pt-BR": "Português", ru: "Русский", tr: "Türkçe", vi: "Tiếng Việt", "zh-CN": "简体中文", "zh-TW": "繁體中文" }`

**Key Imports:** `@roo-code/types`

---

### src\shared\mcp.ts
**Purpose:** Defines types related to MCP server interactions and data.

**Exported Types:**
- `type McpErrorEntry`: message: string, timestamp: number, level: "error" | "warn" | "info"
- `type McpServer`: name: string, config: string, status: "connected" | "connecting" | "disconnected"
- `type McpTool`: name: string, description?: string, inputSchema?: object
- `type McpResource`: uri: string, name: string, mimeType?: string
- `type McpResourceTemplate`: uriTemplate: string, name: string, description?: string
- `type McpResourceResponse`: contents: Array<{ uri: string; mimeType?: string; text?: string; blob?: string; }>
- `type McpToolCallResponse`: content: Array<| { type: "text"; text: string; } | { type: "image"; data: string; mimeType: string; } | { type: "audio"; data: string; mimeType: string; } | { type: "resource"; resource: { uri: string; mimeType?: string; text?: string; blob?: string; }; }>

---

### src\shared\modes.ts
**Purpose:** Manages modes, tool groups, and file matching logic.

**Exported Types:**
- `type Mode`

**Key Imports:** `vscode`, `@roo-code/types`, `../core/prompts/sections/custom-instructions`, `./experiments`, `./tools`

---

### src\shared\package.ts
**Purpose:** Provides access to package metadata, handling environment overrides.

**Exported Constants:**
- `Package` = `{ publisher: publisher, name: process.env.PKG_NAME || name, version: process.env.PKG_VERSION || version, outputChannel: process.env.PKG_OUTPUT_CHANNEL || "Roo-Code", sha: process.env.PKG_SHA }`

**Key Imports:** `../package.json`

---

### src\shared\ProfileValidator.ts
**Purpose:** Validates if a profile is allowed based on organization allow lists.

**Exported Functions:**
- `isProfileAllowedprofile: ProviderSettings, allowList: OrganizationAllowList` → `boolean`

**Exported Types:**
- `class ProfileValidator`

**Key Imports:** `type { ProviderSettings, OrganizationAllowList } from "@roo-code/types"`

---

### src\shared\safeJsonParse.ts
**Purpose:** Safely parses JSON strings, returning a default value on failure.

**Exported Functions:**
- `safeJsonParsejsonString: string | null | undefined, defaultValue?: T` → `T | undefined`

---

### src\shared\support-prompt.ts
**Purpose:** Generates and configures support prompts based on templates and parameters.

**Exported Functions:**
- `createPrompttemplate: string, params: PromptParams` → `string`
- `generateDiagnosticTextdiagnostics?: any[]` → `string`

**Exported Types:**
- `type PromptParams`
- `interface SupportPromptConfig`: template
- `type SupportPromptType`

**Exported Constants:**
- `supportPromptConfigs` = `{
	ENHANCE: { template: `Generate an enhanced version of this prompt (reply with only the enhanced prompt - no conversa``

---

### src\shared\todo.ts
**Purpose:** Extracts the latest todo list from Cline messages.

**Exported Functions:**
- `getLatestTodoclineMessages: ClineMessage[]` → `any[]`

**Key Imports:** `import { ClineMessage } from "@roo-code/types"`

---

### src\shared\tools.ts
**Purpose:** Defines types and interfaces for tool interactions and responses.

**Exported Types:**
- `type ToolResponse`
- `type AskApproval`
- `type HandleError`
- `type PushToolResult`
- `type RemoveClosingTag`
- `type AskFinishSubTaskApproval`
- `type ToolDescription`
- `interface TextContent`: type, content, partial
- `type ToolParamName`
- `interface ToolUse`: type, name

**Exported Constants:**
- `toolParamNames` = `[
	"command",
	"path",
	"content",
	"line_count",
	"regex",
	"file_pattern",
	"recursive",
	"action",
	"url",
	"coordinate",
	"text",
	"server_name",
	"tool_name",
	"arguments",
	"uri",
	"question",
	"result",
	"diff",
	"mode_slug",
	"reason",
	"line",
	"mode",
	"message",
	"cwd",
	"follow_up",
	"task",
	"size",
	"search",
	"replace",
	"use_regex",
	"ignore_case",
	"args",
	"start_line",
	"end_line",
	"query",
	"args",
	"todos",
	"prompt",
	"image",
] as const`

**Key Imports:** `import { Anthropic } from "@anthropic-ai/sdk"`, `import type { ClineAsk, ToolProgressStatus, ToolGroup, ToolName } from "@roo-code/types"`

---

### src\shared\utils\__tests__\requesty.spec.ts
---

### src\shared\utils\requesty.ts
**Purpose:** Constructs Requesty service URLs with validation and fallback mechanisms.

**Exported Functions:**
- `toRequestyServiceUrlbaseUrl?: string | null, service: URLType = "router"` → `string`

**Exported Types:**
- `type URLType`

**Exported Constants:**
- `REQUESTY_BASE_URL` = `"https://router.requesty.ai/v1"`

---

### src\shared\vsCodeSelectorUtils.ts
**Purpose:** Formats VS Code language model selectors into string representations.

**Exported Functions:**
- `stringifyVsCodeLmModelSelectorselector: LanguageModelChatSelector` → `string`

**Exported Constants:**
- `SELECTOR_SEPARATOR` = `"/"`

**Key Imports:** `import { LanguageModelChatSelector } from "vscode"`

---

### src\shared\WebviewMessage.ts
**Purpose:** Defines message types and payloads for webview communication.

**Exported Types:**
- `type ClineAskResponse`
- `type PromptMode`
- `type AudioType`
- `interface UpdateTodoListPayload`: todos
- `type EditQueuedMessagePayload`
- `interface WebviewMessage`: type

**Key Imports:** `import { z } from "zod"`, `import { type ProviderSettings, type PromptComponent, type ModeConfig, type InstallMarketplaceItemOptions, type MarketplaceItem, type ShareVisibility, type QueuedMessage, marketplaceItemSchema } from "@roo-code/types"`, `import { Mode } from "./modes"`

---

### src\utils\__tests__\autoImportSettings.spec.ts
**Purpose:** Tests auto-import settings functionality within the extension.

**Key Imports:** `../autoImportSettings`

---

### src\utils\__tests__\config.spec.ts
**Purpose:** Tests environment variable injection into configuration strings and objects.

**Key Imports:** `../config`

---

### src\utils\__tests__\cost.spec.ts
**Purpose:** Tests API cost calculation for Anthropic and OpenAI models.

**Key Imports:** `@roo-code/types`, `../../shared/cost`

---

### src\utils\__tests__\enhance-prompt.spec.ts
**Purpose:** Tests prompt enhancement using default and custom enhancement prompts.

**Key Imports:** `@roo-code/types`, `../single-completion-handler`, `../../api`, `../../shared/support-prompt`

---

### src\utils\__tests__\git.spec.ts
**Purpose:** Tests Git-related utility functions for repository information.

**Key Imports:** `child_process`, `fs`, `path`, `../git`, `../../integrations/misc/extract-text`

---

### src\utils\__tests__\migrateSettings.spec.ts
**Purpose:** Tests the settings migration process within the extension.

**Key Imports:** `vscode`, `../migrateSettings`

---

### src\utils\__tests__\object.spec.ts
**Purpose:** Tests the `isEmpty` function for various data types.

**Key Imports:** `../object`

---

### src\utils\__tests__\outputChannelLogger.spec.ts
**Purpose:** Tests the output channel logger for logging messages and errors.

**Key Imports:** `vscode`, `../outputChannelLogger`

---

### src\utils\__tests__\path.spec.ts
**Purpose:** Tests path utility functions for workspace and file path manipulation.

**Key Imports:** `os`, `path`, `../path`

---

### src\utils\__tests__\safeWriteJson.test.ts
**Purpose:** Tests the safe JSON writing functionality with file system operations.

**Key Imports:** `fs/promises`, `fs`, `stream`, `path`, `os`, `../safeWriteJson`

---

### src\utils\__tests__\shell.spec.ts
**Purpose:** Tests shell detection and configuration retrieval.

**Key Imports:** `vscode`, `os`, `path`, `../shell`

---

### src\utils\__tests__\storage.spec.ts
**Purpose:** Tests storage path retrieval with custom path configuration.

**Key Imports:** `vscode`, `fs/promises`, `../storage`

---

### src\utils\__tests__\text-normalization.spec.ts
**Purpose:** Tests text normalization utilities for smart quotes and whitespace.

**Key Imports:** `../text-normalization`

---

### src\utils\__tests__\tiktoken.spec.ts
**Purpose:** Tests token counting using the tiktoken library.

**Key Imports:** `../tiktoken`, `@anthropic-ai/sdk`

---

### src\utils\__tests__\xml-matcher.spec.ts
---

### src\utils\__tests__\xml.spec.ts
**Functions:** `toBe`

---

### src\utils\autoImportSettings.ts
**Purpose:** Automatically imports settings from a specified path if it exists.

**Exported Functions:**
- `autoImportSettingsvscode.OutputChannel, { providerSettingsManager, contextProxy, customModesManager }: ImportOptions` → `Promise<void>`
- `resolvePathstring` → `string`

**Key Imports:** `vscode`, `path`, `os`, `../shared/package`, `./fs`, `../i18n`, `../core/config/importExport`

---

### src\utils\commands.ts
**Purpose:** Provides utility functions for generating command identifiers.

**Exported Functions:**
- `getCommandCommandId` → `string`
- `getCodeActionCommandCodeActionId` → `string`
- `getTerminalCommandTerminalActionId` → `string`

**Key Imports:** `@roo-code/types`, `../shared/package`

---

### src\utils\config.ts
**Purpose:** Injects environment variables into configuration objects.

**Exported Functions:**
- `injectEnvC, any` → `Promise<any>`
- `injectVariablesC, Record<string, undefined | null | string | Record<string, undefined | null | string>>, any` → `Promise<any>`

**Exported Types:**
- `type InjectableConfigType`: string, [key: string]

---

### src\utils\countTokens.ts
**Purpose:** Counts tokens in content using worker pool or tiktoken directly.

**Exported Functions:**
- `countTokensAnthropic.Messages.ContentBlockParam[], { useWorker = true }: CountTokensOptions` → `Promise<number>`

**Exported Types:**
- `type CountTokensOptions`: useWorker

**Key Imports:** `@anthropic-ai/sdk`, `workerpool`, `../workers/types`, `./tiktoken`

---

### src\utils\errors.ts
**Purpose:** Defines a custom error for organization allow list violations.

**Exported Types:**
- `class OrganizationAllowListViolationError`: message

---

### src\utils\focusPanel.ts
**Purpose:** Focuses the active panel (tab or sidebar) in VS Code.

**Exported Functions:**
- `focusPanelvscode.WebviewPanel | undefined, vscode.WebviewView | undefined` → `Promise<void>`

**Key Imports:** `vscode`, `../shared/package`, `../core/webview/ClineProvider`

---

### src\utils\fs.ts
**Purpose:** Provides asynchronous file system utility functions.

**Exported Functions:**
- `createDirectoriesForFilestring` → `Promise<string[]>`
- `fileExistsAtPathstring` → `Promise<boolean>`

**Key Imports:** `fs/promises`, `path`

---

### src\utils\git.ts
**Purpose:** Provides utility functions for interacting with Git repositories.

**Exported Functions:**
- `getGitRepositoryInfostring` → `Promise<GitRepositoryInfo>`
- `convertGitUrlToHttpsstring` → `string`
- `sanitizeGitUrlstring` → `string`
- `extractRepositoryNamestring` → `string`
- `getWorkspaceGitInfovscode.WorkspaceFolder` → `Promise<GitRepositoryInfo | undefined>`
- `checkGitRepostring` → `Promise<boolean>`
- `checkGitInstalled` → `Promise<boolean>`
- `searchCommitsstring, string, number` → `Promise<GitCommit[]>`
- `getCommitInfostring, string` → `Promise<GitCommit | undefined>`
- `getWorkingStatestring` → `Promise<string | undefined>`

**Exported Types:**
- `interface GitRepositoryInfo`: repositoryUrl, repositoryName, defaultBranch
- `interface GitCommit`: hash, shortHash, subject, author

**Key Imports:** `vscode`, `path`, `fs`, `child_process`, `util`, `../integrations/misc/extract-text`

---

### src\utils\globalContext.ts
**Purpose:** Provides functions to manage global storage paths.

**Exported Functions:**
- `getGlobalFsPathExtensionContext` → `Promise<string>`
- `ensureSettingsDirectoryExistsExtensionContext` → `Promise<string>`

**Key Imports:** `fs/promises`, `path`, `vscode`

---

### src\utils\logging\__tests__\CompactLogger.spec.ts
**Purpose:** Tests the CompactLogger's log levels and metadata handling.

**Exported Functions:**
- `constructor` → ``

**Key Imports:** `../CompactLogger`, `./MockTransport`, `../types`, `vitest`, `../CompactTransport`

---

### src\utils\logging\__tests__\CompactTransport.spec.ts
**Purpose:** Tests the CompactTransport's file handling and log writing capabilities.

**Exported Functions:**
- `cleanupTestLogs` → ``
- `rmDirRecursivedirPath: string` → ``

**Key Imports:** `../CompactTransport`, `fs`, `path`, `vitest`

---

### src\utils\logging\__tests__\MockTransport.ts
**Purpose:** Provides a mock transport for testing logging functionality.

**Exported Types:**
- `class MockTransport`: entries: CompactLogEntry[], closed: boolean, constructor(), write(entry: CompactLogEntry): Promise<void>, close(): Promise<void>

**Exported Constants:**
- `TEST_CONFIG` = `{ level: "fatal", fileOutput: { enabled: false, path: "" } }`

**Key Imports:** `../CompactTransport`, `../types`

---

### src\utils\logging\CompactLogger.ts
**Purpose:** Implements a compact logger with efficient logging capabilities.

**Exported Types:**
- `interface ILogger`: debug, info, warn, error

**Key Imports:** `./types`, `./CompactTransport`

---

### src\utils\logging\CompactTransport.ts
**Purpose:** Implements compact logging transport with file output support.

**Exported Types:**
- `type CompactTransportConfig`: level, fileOutput
- `interface ICompactTransport`: write

**Key Imports:** `fs`, `path`, `./types`

---

### src\utils\logging\index.ts
**Purpose:** Provides a default logger instance with Jest environment detection.

**Exported Constants:**
- `logger` = `process.env.NODE_ENV === "test" ? new CompactLogger() : noopLogger`

**Key Imports:** `./CompactLogger`

---

### src\utils\logging\types.ts
**Purpose:** Defines core type definitions for the compact logging system.

**Exported Types:**
- `interface CompactLogEntry`: t, l, m, c
- `type LogLevel`
- `interface LogMeta`: ctx
- `interface CompactTransportConfig`: level, fileOutput
- `interface ICompactTransport`: write

---

### src\utils\migrateSettings.ts
**Purpose:** Migrates legacy settings files to new file names and formats.

**Exported Functions:**
- `migrateSettingscontext: vscode.ExtensionContext, outputChannel: vscode.OutputChannel` → `Promise<void>`
- `migrateCustomModesToYaml` → ``
- `migrateDefaultCommandscontext: vscode.ExtensionContext, outputChannel: vscode.OutputChannel` → `Promise<void>`

**Key Imports:** `vscode`, `path`, `fs/promises`, `./fs`, `../shared/globalFileNames`, `yaml`

---

### src\utils\object.ts
**Purpose:** Checks if an object is empty by examining its properties.

**Exported Functions:**
- `isEmptyobj: unknown` → `boolean`

---

### src\utils\outputChannelLogger.ts
**Purpose:** Creates logging functions that write to VSCode output channels.

**Exported Types:**
- `type LogFunction`

**Key Imports:** `vscode`

---

### src\utils\path.ts
**Purpose:** Provides utilities for consistent path handling and presentation.

**Exported Functions:**
- `toPosixPath` → ``
- `arePathsEqual` → ``
- `normalizePath` → ``
- `getReadablePath` → ``
- `toRelativePath` → ``
- `getWorkspacePath` → ``

**Key Imports:** `path`, `os`, `vscode`

---

### src\utils\pathUtils.ts
**Purpose:** Determines if a given file path resides outside of workspaces.

**Exported Functions:**
- `isPathOutsideWorkspacefilePath: string` → `boolean`

**Key Imports:** `vscode`, `path`

---

### src\utils\safeWriteJson.ts
**Purpose:** Safely writes JSON data to a file with locking and backup features.

**Exported Functions:**
- `safeWriteJsonfilePath: string, data: any` → `Promise<void>`
- `_streamDataToFile` → ``
- `releaseLock` → ``
- `handleError` → ``

**Key Imports:** `fs/promises`, `fs`, `path`, `proper-lockfile`, `stream-json/Disassembler`, `stream-json/Stringer`

---

### src\utils\shell.ts
**Purpose:** Provides shell-related utilities, including shell path normalization and validation.

**Exported Functions:**
- `getWindowsTerminalConfig` → ``
- `getMacTerminalConfig` → ``
- `getLinuxTerminalConfig` → ``
- `normalizeShellPath` → ``
- `getWindowsShellFromVSCode` → ``
- `getMacShellFromVSCode` → ``
- `getLinuxShellFromVSCode` → ``
- `getShellFromUserInfo` → ``
- `getShellFromEnv` → ``
- `isShellAllowed` → ``
- `getSafeFallbackShell` → ``
- `getShell` → ``

**Exported Constants:**
- `SHELL_ALLOWLIST` = `Set<string>`

**Key Imports:** `vscode`, `os`, `path`

---

### src\utils\single-completion-handler.ts
**Purpose:** Enhances prompts using the API for single completion requests.

**Exported Functions:**
- `singleCompletionHandlerapiConfiguration: ProviderSettings, promptText: string` → `Promise<string>`

**Key Imports:** `type { ProviderSettings } from "@roo-code/types"`, `../api`

---

### src\utils\storage.ts
**Purpose:** Manages storage paths, including custom and default VSCode storage.

**Exported Functions:**
- `getStorageBasePathdefaultPath: string` → `Promise<string>`
- `getTaskDirectoryPath` → ``
- `getSettingsDirectoryPath` → ``
- `getCacheDirectoryPath` → ``
- `promptForCustomStoragePath` → ``

**Key Imports:** `vscode`, `path`, `fs/promises`, `fs`, `../shared/package`, `../i18n`

---

### src\utils\text-normalization.ts
**Purpose:** Provides string normalization with various character replacement options.

**Exported Types:**
- `interface NormalizeOptions`: smartQuotes?: boolean, typographicChars?: boolean, extraWhitespace?: boolean, trim?: boolean

**Exported Constants:**
- `NORMALIZATION_MAPS` = `{ SMART_QUOTES: { ... }, TYPOGRAPHIC: { ... } }`

---

### src\utils\tiktoken.ts
**Purpose:** Estimates token counts for Anthropic messages using tiktoken.

**Exported Functions:**
- `tiktokencontent: Anthropic.Messages.ContentBlockParam[]` → `Promise<number>`

**Key Imports:** `Anthropic`, `Tiktoken`, `tiktoken/lite`, `tiktoken/encoders/o200k_base`

---

### src\utils\tts.ts
**Purpose:** Manages text-to-speech functionality, including enabling, speed, and queueing.

**Exported Functions:**
- `setTtsEnabledenabled: boolean` → ``
- `setTtsSpeednewSpeed: number` → ``
- `playTtsmessage: string, options: PlayTtsOptions = {}` → `Promise<void>`
- `stopTts` → ``

---

### src\utils\vitest-verbosity.ts
**Purpose:** Resolves verbosity settings for Vitest based on command-line arguments.

**Exported Functions:**
- `resolveVerbosityargv = process.argv, env = process.env` → ``

---

### src\utils\xml-matcher.ts
**Purpose:** Provides a class for matching XML tags and extracting data.

**Exported Types:**
- `interface XmlMatcherResult`: matched: boolean, data: string
- `class XmlMatcher`: index: number, chunks: XmlMatcherResult[], cached: string[], matched: boolean, state: "TEXT" | "TAG_OPEN" | "TAG_CLOSE", depth: number, pointer: number, constructor(tagName: string, transform?: (chunks: XmlMatcherResult) => Result, position = 0)

---

### src\utils\xml.ts
**Purpose:** Parses XML strings into JavaScript objects using specified options.

**Exported Functions:**
- `parseXmlxmlString: string, stopNodes?: string[], options?: ParseXmlOptions` → `unknown`

**Exported Types:**
- `interface ParseXmlOptions`: processEntities?: boolean

**Key Imports:** `fast-xml-parser`

---

### src\vitest.config.ts
---

### src\vitest.setup.ts
**Functions:** `allowNetConnect`

---

### src\workers\countTokens.ts
**Purpose:** Counts tokens in content using tiktoken and Anthropic SDK.

**Exported Functions:**
- `countTokensAnthropic.Messages.ContentBlockParam[]` → `Promise<CountTokensResult>`

**Key Imports:** `workerpool`, `@anthropic-ai/sdk`, `../utils/tiktoken`, `./types`

---

### src\workers\types.ts
**Purpose:** Defines the schema and type for the token counting result.

**Exported Types:**
- `type CountTokensResult`: success, count, error

**Key Imports:** `zod`

---

### webview-ui\src\__tests__\App.spec.tsx
**Purpose:** Tests the rendering and behavior of the main application component.

**Exported Functions:**
- `ChatView{ isHidden: boolean }` → `any`
- `SettingsView{ onDone: () => void }` → `any`
- `HistoryView{ onDone: () => void }` → `any`
- `McpView` → `any`
- `ModesView` → `any`
- `MarketplaceView` → `any`
- `CloudView` → `any`
- `tFunctionkey: string` → `any`
- `MockedComponentprops: any` → `any`
- `triggerMessage` → `any`

**Key Imports:** `react`, `@/utils/test-utils`, `../App`, `@src/utils/vscode`, `@src/components/ErrorBoundary`

---

### webview-ui\src\__tests__\command-autocomplete.spec.ts
**Purpose:** Tests command suggestions for slash command autocompletion.

**Key Imports:** `type { Command } from "@roo/ExtensionMessage"`, `../utils/context-mentions`

---

### webview-ui\src\__tests__\ContextWindowProgress.spec.tsx
**Purpose:** Tests the ContextWindowProgress component's rendering and behavior.

**Key Imports:** `@/utils/test-utils`, `@tanstack/react-query`, `@src/components/chat/TaskHeader`, `@/utils/format`

---

### webview-ui\src\__tests__\ContextWindowProgressLogic.spec.ts
**Purpose:** Tests the logic behind the ContextWindowProgress component's calculations.

**Key Imports:** `@src/utils/model-utils`

---

### webview-ui\src\__tests__\ErrorBoundary.spec.tsx
**Purpose:** Tests the ErrorBoundary component's error handling and rendering.

**Exported Functions:**
- `tFunctionkey: string` → `any`
- `MockedComponentprops: any` → `any`
- `ErrorThrower{ shouldThrow?: boolean; message?: string }` → `any`

**Key Imports:** `react`, `@testing-library/react`, `../components/ErrorBoundary`, `@src/utils/TelemetryClient`, `react-i18next`

---

### webview-ui\src\__tests__\SearchableSelect.spec.tsx
**Purpose:** Tests the SearchableSelect component's functionality and rendering.

**Key Imports:** `react`, `@/utils/test-utils`, `@/components/ui/searchable-select`, `@testing-library/user-event`

---

### webview-ui\src\__tests__\TelemetryClient.spec.ts
**Purpose:** Tests the TelemetryClient's singleton pattern and update methods.

**Key Imports:** `posthog`, `@src/utils/TelemetryClient`

---

### webview-ui\src\App.tsx
**Purpose:** Renders the main application, managing state and UI components.

**Exported Functions:**
- `App` → `JSX.Element`
- `AppWithProviders` → `JSX.Element`

**Key Imports:** `react`, `react-use`, `@tanstack/react-query`, `@roo/ExtensionMessage`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\__tests__\ErrorBoundary.spec.tsx
**Purpose:** Tests the ErrorBoundary component's error handling and rendering.

**Exported Functions:**
- `ErrorThrowingComponent({ shouldThrow = false })` → `any`

**Key Imports:** `react`, `@testing-library/react`, `../ErrorBoundary`, `@src/utils/TelemetryClient`, `react-i18next`

---

### webview-ui\src\components\chat\__tests__\ApiConfigSelector.spec.tsx
**Purpose:** Tests the ApiConfigSelector component's functionality.

**Key Imports:** `@/utils/test-utils`, `@/utils/vscode`, `../ApiConfigSelector`, `@/i18n/TranslationContext`, `@/components/ui/hooks/useRooPortal`

---

### webview-ui\src\components\chat\__tests__\BatchFilePermission.spec.tsx
**Purpose:** Tests the BatchFilePermission component's file list rendering.

**Key Imports:** `react`, `@/utils/test-utils`, `@/i18n/__mocks__/TranslationContext`, `../BatchFilePermission`

---

### webview-ui\src\components\chat\__tests__\ChatRow.run-slash-command.spec.tsx
**Purpose:** Tests ChatRow's slash command execution functionality and rendering.

**Exported Functions:**
- `renderChatRowWithProvidersmessage: any, isExpanded = false` → `any`

**Key Imports:** `react`, `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\ChatTextArea.spec.tsx
**Purpose:** Tests the ChatTextArea component's enhance prompt button and dropdown.

**Exported Functions:**
- `getEnhancePromptButton` → `any`
- `getApiConfigDropdown` → `any`

**Key Imports:** `@roo/modes`, `@src/utils/test-utils`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\__tests__\ChatView.auto-approve-new.spec.tsx
**Purpose:** Tests ChatView component's auto-approve functionality with new messages.

**Exported Functions:**
- `MockBrowserSessionRow{ messages }: { messages: any[] }` → `any`
- `MockChatRow{ message }: { message: any }` → `any`
- `MockTaskHeader{ task }: { task: any }` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Key Imports:** `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`, `../ChatView`

---

### webview-ui\src\components\chat\__tests__\ChatView.auto-approve.spec.tsx
**Purpose:** Tests ChatView component's auto-approve functionality.

**Exported Functions:**
- `MockBrowserSessionRow{ messages }: { messages: any[] }` → `any`
- `MockChatRow{ message }: { message: any }` → `any`
- `MockTaskHeader{ task }: { task: any }` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Key Imports:** `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`, `../ChatView`

---

### webview-ui\src\components\chat\__tests__\ChatView.keyboard-fix.spec.tsx
**Purpose:** Tests ChatView component's keyboard interaction and fixes.

**Exported Functions:**
- `MockChatTextArea` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Key Imports:** `react`, `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\__tests__\ChatView.spec.tsx
**Purpose:** Tests the ChatView component's rendering and behavior.

**Exported Functions:**
- `MockBrowserSessionRow{ messages }: { messages: ClineMessage[] }` → `any`
- `MockChatRow{ message }: { message: ClineMessage }` → `any`
- `MockAnnouncement` → `any`
- `MockDismissibleUpsell` → `any`
- `MockQueuedMessages` → `any`
- `MockRooTips` → `any`
- `MockRooHero` → `any`
- `MockTelemetryBanner` → `any`
- `MockChatTextArea` → `any`
- `MockVSCodeButton` → `any`
- `MockVSCodeTextField` → `any`
- `MockVSCodeLink` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Exported Types:**
- `interface ClineMessage`: type, say?, ask?, ts, text?, partial?
- `interface ExtensionState`: version, clineMessages, taskHistory, shouldShowAnnouncement, allowedCommands, alwaysAllowExecute

**Key Imports:** `react`, `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\__tests__\CheckpointRestoreDialog.spec.tsx
**Purpose:** Tests the CheckpointRestoreDialog component's rendering and behavior.

**Key Imports:** `react`, `@/utils/test-utils`, `vitest`

---

### webview-ui\src\components\chat\__tests__\CloudTaskButton.spec.tsx
**Purpose:** Tests the CloudTaskButton component's functionality and rendering.

**Key Imports:** `react-i18next`, `@/utils/test-utils`, `qrcode`, `@roo-code/cloud/src/config`, `@/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\CommandExecution.spec.tsx
**Purpose:** Tests the CommandExecution component's command execution behavior.

**Exported Functions:**
- `ExtensionStateWrapper{ children }: { children: React.ReactNode }` → `any`

**Key Imports:** `react`, `@testing-library/react`, `../CommandExecution`, `../../../context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\CommandPatternSelector.spec.tsx
**Purpose:** Tests the CommandPatternSelector component's rendering and interaction.

**Exported Functions:**
- `TestWrapper{ children }: { children: React.ReactNode }` → `any`

**Key Imports:** `react`, `@testing-library/react`, `../CommandPatternSelector`, `../../../components/ui/tooltip`

---

### webview-ui\src\components\chat\__tests__\FollowUpSuggest.spec.tsx
**Purpose:** Tests the FollowUpSuggest component's rendering and functionality.

**Exported Functions:**
- `renderWithTestProviders` → `any`

**Exported Types:**
- `interface TestExtensionState`: autoApprovalEnabled, alwaysAllowFollowupQuestions, followupAutoApproveTimeoutMs

**Key Imports:** `react`, `@testing-library/react`, `@radix-ui/react-tooltip`, `../FollowUpSuggest`

---

### webview-ui\src\components\chat\__tests__\IndexingStatusBadge.spec.tsx
**Purpose:** Tests the IndexingStatusBadge component's rendering and behavior.

**Exported Functions:**
- `renderComponent` → `any`

**Key Imports:** `react`, `@/utils/test-utils`, `@src/utils/vscode`, `../IndexingStatusBadge`

---

### webview-ui\src\components\chat\__tests__\ModeSelector.spec.tsx
**Purpose:** Tests the ModeSelector component's rendering and mode selection.

**Key Imports:** `@/utils/test-utils`, `@roo-code/types`, `@roo/modes`, `../ModeSelector`

---

### webview-ui\src\components\chat\__tests__\ShareButton.spec.tsx
**Purpose:** Tests the ShareButton component's rendering and behavior.

**Key Imports:** `react-i18next`, `@/utils/test-utils`, `@/utils/vscode`, `../ShareButton`, `@/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\SlashCommandItemSimple.spec.tsx
**Purpose:** Tests the SlashCommandItemSimple component's rendering and actions.

**Key Imports:** `@/utils/test-utils`, `@roo/ExtensionMessage`, `../SlashCommandItemSimple`

---

### webview-ui\src\components\chat\__tests__\TaskActions.spec.tsx
**Purpose:** Tests the TaskActions component's rendering and event handling.

**Key Imports:** `@roo-code/types`, `@/utils/test-utils`, `@/utils/vscode`, `@/context/ExtensionStateContext`, `../TaskActions`

---

### webview-ui\src\components\chat\__tests__\TaskHeader.spec.tsx
**Purpose:** Tests the TaskHeader component's rendering and state management.

**Key Imports:** `react`, `@/utils/test-utils`, `@tanstack/react-query`, `@roo-code/types`, `../TaskHeader`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\chat\Announcement.tsx
**Purpose:** Displays announcements within the chat interface, handling visibility.

**Exported Functions:**
- `AnnouncementAnnouncementProps` → `JSX.Element`
- `XLink` → `JSX.Element`
- `DiscordLink` → `JSX.Element`
- `RedditLink` → `JSX.Element`

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo/package`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\chat\ApiConfigSelector.tsx
**Purpose:** Provides a selector component for choosing API configurations.

**Exported Functions:**
- `ApiConfigSelectorApiConfigSelectorProps` → `JSX.Element`

**Key Imports:** `react`, `fzf`, `@/lib/utils`, `@/components/ui`, `@/i18n/TranslationContext`, `@/utils/vscode`

---

### webview-ui\src\components\chat\AutoApprovedRequestLimitWarning.tsx
**Purpose:** Displays a warning when auto-approved request limits are reached.

**Exported Functions:**
- `AutoApprovedRequestLimitWarning({ message }: AutoApprovedRequestLimitWarningProps)` → `JSX.Element | null`

**Exported Types:**
- `type AutoApprovedRequestLimitWarningProps`: message: ClineMessage

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `react-i18next`, `@roo-code/types`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\AutoApproveDropdown.tsx
**Purpose:** Renders a dropdown for managing auto-approval settings.

**Exported Functions:**
- `AutoApproveDropdown({ disabled = false, triggerClassName = "" }: AutoApproveDropdownProps)` → `JSX.Element`

**Exported Types:**
- `interface AutoApproveDropdownProps`: disabled?: boolean, triggerClassName?: string

**Key Imports:** `react`, `lucide-react`, `@/utils/vscode`, `@/context/ExtensionStateContext`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\chat\BatchDiffApproval.tsx
**Purpose:** Displays and expands file diffs in an accordian for batch approval.

**Exported Functions:**
- `BatchDiffApproval({ files = [], ts }: BatchDiffApprovalProps)` → `JSX.Element | null`

**Exported Types:**
- `interface FileDiff`: path: string, changeCount: number, key: string, content: string, diffs?: Array<{ content: string; startLine?: number; }>
- `interface BatchDiffApprovalProps`: files: FileDiff[], ts: number

**Key Imports:** `react`, `../common/CodeAccordian`

---

### webview-ui\src\components\chat\BatchFilePermission.tsx
**Purpose:** Renders file permission requests for batch approval.

**Exported Functions:**
- `BatchFilePermission({ files = [], onPermissionResponse, ts }: BatchFilePermissionProps)` → `JSX.Element | null`

**Exported Types:**
- `interface FilePermissionItem`: path: string, lineSnippet?: string, isOutsideWorkspace?: boolean, key: string, content?: string
- `interface BatchFilePermissionProps`: files: FilePermissionItem[], onPermissionResponse?: (response: { [key: string]: boolean }) => void, ts: number

**Key Imports:** `react`, `../common/ToolUseBlock`, `@src/utils/vscode`, `@src/utils/removeLeadingNonAlphanumeric`

---

### webview-ui\src\components\chat\BrowserSessionRow.tsx
**Purpose:** Displays browser session messages with actions and results.

**Exported Functions:**
- `BrowserSessionRowContent(props: BrowserSessionRowProps)` → `JSX.Element`
- `BrowserActionBox(props: { action: BrowserAction; result?: BrowserActionResult; messageTs: number; })` → `JSX.Element`
- `getBrowserActionText(action: BrowserAction, result?: BrowserActionResult)` → `string`

**Exported Types:**
- `interface BrowserSessionRowProps`: messages: ClineMessage[], isExpanded: (messageTs: number) => boolean, onToggleExpand: (messageTs: number) => void, lastModifiedMessage?: ClineMessage, isLast: boolean, onHeightChange: (isTaller: boolean) => void, isStreaming: boolean

**Key Imports:** `react`, `react-use`, `fast-deep-equal`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\chat\ChatRow.tsx
**Purpose:** Renders individual chat messages with various content types.

**Exported Functions:**
- `ChatRowContent(props: ChatRowContentProps)` → `JSX.Element`
- `handleMessage(message: ClineMessage, isLast: boolean, isStreaming: boolean)` → `JSX.Element`
- `getIconSpan(message: ClineMessage)` → `JSX.Element`
- `toolIcon(message: ClineMessage)` → `JSX.Element`

**Exported Types:**
- `interface ChatRowContentProps`: message: ClineMessage, isLast: boolean, isStreaming: boolean, isExpanded: boolean, onToggleExpand: () => void, onHeightChange: (isTaller: boolean) => void

**Key Imports:** `react`, `react-use`, `react-i18next`, `fast-deep-equal`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\chat\ChatTextArea.tsx
**Purpose:** Provides a text area for composing and sending chat messages.

**Exported Functions:**
- `handleClickOutside(event: MouseEvent)` → `void`
- `messageHandler(message: string, mode: Mode)` → `void`

**Key Imports:** `react`, `react-use`, `react-textarea-autosize`, `lucide-react`, `@roo/context-mentions`, `@roo/WebviewMessage`

---

### webview-ui\src\components\chat\ChatView.tsx
**Purpose:** Manages the display and interaction of the chat interface.

**Exported Functions:**
- `playSound(sound: string)` → `void`
- `playTts(text: string, voice?: string)` → `void`
- `getAudioUrl(audioType: AudioType, audioId: string)` → `string`
- `endBrowserSession()` → `void`
- `autoApproveOrReject(message: ClineAsk, approve: boolean)` → `void`
- `handleCondenseContext(message: ClineMessage)` → `void`

**Key Imports:** `react`, `react-use`, `debounce`, `react-virtuoso`, `remove-markdown`, `@vscode/webview-ui-toolkit/react`, `use-sound`, `lru-cache`, `react-i18next`, `@src/utils/useDebounceEffect`

---

### webview-ui\src\components\chat\CheckpointRestoreDialog.tsx
**Purpose:** Displays a dialog for restoring or discarding checkpoints.

**Exported Functions:**
- `CheckpointRestoreDialog({ open, onOpenChange, onConfirm, type, hasCheckpoint }: CheckpointRestoreDialogProps)` → `JSX.Element`

**Exported Types:**
- `interface CheckpointRestoreDialogProps`: open: boolean, onOpenChange: (open: boolean) => void, onConfirm: (restoreCheckpoint: boolean) => void, type: "edit" | "delete", hasCheckpoint: boolean

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\chat\checkpoints\__tests__\CheckpointSaved.spec.tsx
**Functions:** `waitForOpenHandler`, `getMenu`, `popoverRoot`, `menuContainer`

---

### webview-ui\src\components\chat\checkpoints\CheckpointMenu.tsx
**Purpose:** Renders a menu for checkpoint-related actions.

**Exported Functions:**
- `CheckpointMenu({ ts, commitHash, currentHash, checkpoint, open, onOpenChange }: CheckpointMenuProps)` → `JSX.Element`

**Exported Types:**
- `type CheckpointMenuBaseProps`: ts: number, commitHash: string, currentHash?: string, checkpoint: Checkpoint
- `type CheckpointMenuControlledProps`: open: boolean, onOpenChange: (open: boolean) => void
- `type CheckpointMenuUncontrolledProps`: open?: undefined, onOpenChange?: undefined
- `type CheckpointMenuProps`

**Key Imports:** `react`, `@radix-ui/react-icons`, `react-i18next`, `../components/ui`, `@src/utils/vscode`, `./schema`

---

### webview-ui\src\components\chat\checkpoints\CheckpointSaved.tsx
**Purpose:** Displays a saved checkpoint indicator with menu options.

**Exported Functions:**
- `CheckpointSaved({ checkpoint, ...props }: CheckpointSavedProps)` → `JSX.Element`
- `handlePopoverOpenChange(open: boolean)` → `void`

**Exported Types:**
- `type CheckpointSavedProps`: ts: number, commitHash: string, currentHash?: string, checkpoint?: Record<string, unknown>

**Key Imports:** `react`, `react-i18next`, `@/lib/utils`, `./CheckpointMenu`, `./schema`, `lucide-react`

---

### webview-ui\src\components\chat\checkpoints\schema.ts
**Purpose:** Defines the schema for checkpoint data using Zod.

**Exported Types:**
- `type Checkpoint`

**Key Imports:** `zod`

---

### webview-ui\src\components\chat\CheckpointWarning.tsx
**Purpose:** Displays a warning message related to checkpoint initialization.

**Exported Functions:**
- `CheckpointWarning()` → `JSX.Element`

**Key Imports:** `react-i18next`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\chat\CloudTaskButton.tsx
**Purpose:** Provides a button for creating and sharing cloud tasks.

**Exported Functions:**
- `CloudTaskButton({ item, disabled = false }: CloudTaskButtonProps)` → `JSX.Element`

**Exported Types:**
- `interface CloudTaskButtonProps`: item?: HistoryItem, disabled?: boolean

**Key Imports:** `react`, `react-i18next`, `lucide-react`, `qrcode`, `@roo-code/types`, `@/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\CodebaseSearchResult.tsx
**Purpose:** Displays a single codebase search result with file details.

**Exported Functions:**
- `handleClick()` → `void`

**Exported Types:**
- `interface CodebaseSearchResultProps`: filePath: string, score: number, startLine: number, endLine: number, snippet: string, language: string

**Key Imports:** `react`, `react-i18next`, `@src/utils/vscode`, `@/components/ui`

---

### webview-ui\src\components\chat\CodebaseSearchResultsDisplay.tsx
**Purpose:** Displays codebase search results with expandable/collapsible functionality.

**Exported Types:**
- `interface CodebaseSearchResultsDisplayProps`: results: Array<{ filePath: string, score: number, startLine: number, endLine: number, codeChunk: string }>

**Key Imports:** `react`, `./CodebaseSearchResult`, `react-i18next`

---

### webview-ui\src\components\chat\CodeIndexPopover.tsx
**Purpose:** Manages and displays the code index settings and indexing status.

**Exported Functions:**
- `createValidationSchema` → ``
- `handleMessage` → ``
- `updateSetting` → ``
- `handleSaveSettings` → ``
- `getAvailableModels` → ``

**Exported Types:**
- `interface EmbedderProvider`: id, name, url, model, providerType
- `interface IndexingStatus`: systemStatus, processedItems, totalItems, currentItemUnit, workspacePath

**Exported Constants:**
- `DEFAULT_QDRANT_URL` = `"http://localhost:6333"`
- `DEFAULT_OLLAMA_URL` = `"http://localhost:11434"`

**Key Imports:** `react`, `react-i18next`, `zod`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\chat\CommandExecution.tsx
**Purpose:** Renders and manages the execution of commands within the chat interface.

**Exported Functions:**
- `CommandExecution(executionId: string, text?: string, icon?: JSX.Element | null, title?: JSX.Element | null)` → ``

**Exported Types:**
- `interface CommandPattern`: pattern: string, description?: string
- `interface CommandExecutionProps`: executionId: string, text?: string, icon?: JSX.Element | null, title?: JSX.Element | null

**Key Imports:** `react`, `react-use`, `@roo-code/types`, `@roo/ExtensionMessage`, `@roo/safeJsonParse`

---

### webview-ui\src\components\chat\CommandExecutionError.tsx
**Purpose:** Displays an error message related to command execution failures.

**Exported Functions:**
- `CommandExecutionError` → ``

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\chat\CommandPatternSelector.tsx
**Purpose:** Provides a selector for managing command patterns and their permissions.

**Exported Functions:**
- `getEditState` → ``
- `setEditState` → ``

**Exported Types:**
- `interface CommandPattern`: pattern: string, description?: string
- `interface CommandPatternSelectorProps`: patterns: CommandPattern[], allowedCommands: string[], deniedCommands: string[], onAllowPatternChange: (pattern: string) => void

**Key Imports:** `react`, `lucide-react`, `../../lib/utils`, `react-i18next`, `../ui/standard-tooltip`

---

### webview-ui\src\components\chat\ContextCondenseRow.tsx
**Purpose:** Displays a row summarizing context condensation details and costs.

**Exported Functions:**
- `ContextCondenseRow(cost: number, prevContextTokens: number, newContextTokens: number, summary: string)` → ``

**Exported Types:**
- `interface ContextCondense`: cost, prevContextTokens, newContextTokens, summary

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\chat\ContextMenu.tsx
**Purpose:** Renders a context menu with options based on search and input.

**Exported Functions:**
- `renderOptionContent` → ``
- `handleSettingsClick` → ``

**Exported Types:**
- `interface ContextMenuProps`: onSelect, searchQuery, inputValue, onMouseDown, selectedIndex

**Key Imports:** `react`, `vscode-material-icons`, `@roo-code/types`, `@roo/ExtensionMessage`, `@src/utils/context-mentions`

---

### webview-ui\src\components\chat\ContextWindowProgress.tsx
**Purpose:** Displays a progress indicator for the context window usage.

**Exported Functions:**
- `ContextWindowProgress(contextWindow: number, contextTokens: number, maxTokens?: number)` → ``

**Exported Types:**
- `interface ContextWindowProgressProps`: contextWindow: number, contextTokens: number, maxTokens?: number

**Key Imports:** `react`, `react-i18next`, `../utils/format`, `../utils/model-utils`, `../components/ui`

---

### webview-ui\src\components\chat\ErrorRow.tsx
**Purpose:** Provides a unified display component for various error types.

**Exported Functions:**
- `getDefaultTitle` → ``
- `ErrorRow(type: "error" | "mistake_limit" | "api_failure" | "diff_error" | "streaming_failed" | "cancelled", title?: string, message: string, showCopyButton?: boolean, expandable?: boolean, defaultExpanded?: boolean, additionalContent?: React.ReactNode, headerClassName?: string, messageClassName?: string)` → ``

**Exported Types:**
- `interface ErrorRowProps`: type, title, message, showCopyButton, expandable

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `../utils/clipboard`, `../common/CodeBlock`

---

### webview-ui\src\components\chat\FollowUpSuggest.tsx
**Purpose:** Renders and manages follow-up suggestions within the chat interface.

**Exported Functions:**
- `FollowUpSuggest(suggestions?: SuggestionItem[], onSuggestionClick?: (suggestion: SuggestionItem, event?: React.MouseEvent) => void, ts: number, onCancelAutoApproval?: () => void, isAnswered?: boolean)` → ``

**Exported Types:**
- `interface FollowUpSuggestProps`: suggestions?: SuggestionItem[], onSuggestionClick?: (suggestion: SuggestionItem, event?: React.MouseEvent) => void, ts: number, onCancelAutoApproval?: () => void

**Key Imports:** `react`, `lucide-react`, `../components/ui`, `@src/i18n/TranslationContext`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\hooks\usePromptHistory.ts
**Purpose:** Manages and provides prompt history functionality for the chat input.

**Exported Functions:**
- `usePromptHistory({ clineMessages, taskHistory, cwd, inputValue, setInputValue }: UsePromptHistoryProps)` → `UsePromptHistoryReturn`

**Exported Types:**
- `interface UsePromptHistoryProps`: clineMessages: ClineMessage[] | undefined, taskHistory: HistoryItem[] | undefined, cwd: string | undefined, inputValue: string
- `interface UsePromptHistoryReturn`: historyIndex, setHistoryIndex, tempInput, setTempInput, promptHistory

**Key Imports:** `react`, `@roo-code/types`

---

### webview-ui\src\components\chat\IconButton.tsx
**Purpose:** Renders a customizable icon button with tooltip and loading state.

**Exported Functions:**
- `IconButton(iconClass: string, title: string, className: string, disabled: boolean, tooltip: boolean, isLoading: boolean, onClick: any, style: any, ...props: any)` → ``

**Exported Types:**
- `interface IconButtonProps`: iconClass: string, title: string, disabled?: boolean, tooltip?: boolean, isLoading?: boolean

**Key Imports:** `../lib/utils`, `../components/ui`

---

### webview-ui\src\components\chat\IndexingStatusBadge.tsx
**Purpose:** Displays an indexing status badge with a popover for details.

**Exported Functions:**
- `handleMessage` → ``

**Exported Types:**
- `interface IndexingStatusBadgeProps`: className?: string

**Key Imports:** `react`, `lucide-react`, `../lib/utils`, `../utils/vscode`, `../i18n/TranslationContext`

---

### webview-ui\src\components\chat\Markdown.tsx
**Purpose:** Renders markdown content with a copy-to-clipboard button.

**Exported Functions:**
- `Markdown(markdown?: string, partial?: boolean)` → ``

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `../utils/clipboard`, `../components/ui`, `../common/MarkdownBlock`

---

### webview-ui\src\components\chat\McpExecution.tsx
**Purpose:** Renders and manages the execution of MCP commands within the chat interface.

**Exported Functions:**
- `McpExecutionexecutionId: string, text?: string, serverName: string, toolName: string, isArguments: boolean, server: any, useMcpServer: any, alwaysAllowMcp: boolean` → `any`

**Exported Types:**
- `interface McpExecutionProps`: executionId: string, text?: string, serverName?: string, toolName?: string, isArguments?: boolean

**Key Imports:** `react`, `lucide-react`, `react-i18next`, `@roo-code/types`, `@src/lib/utils`

---

### webview-ui\src\components\chat\Mention.tsx
**Purpose:** Displays and formats mentions within chat messages, making them interactive.

**Exported Functions:**
- `Mentiontext: string, withShadow: boolean` → `any`

**Exported Types:**
- `interface MentionProps`: text?: string, withShadow?: boolean

**Key Imports:** `@roo/context-mentions`, `../../utils/vscode`

---

### webview-ui\src\components\chat\MessageModificationConfirmationDialog.tsx
**Purpose:** Provides a confirmation dialog for editing or deleting chat messages.

**Exported Types:**
- `interface MessageModificationConfirmationDialogProps`: open: boolean, onOpenChange: (open: boolean) => void, onConfirm: () => void, type: "edit" | "delete"

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\chat\ModeSelector.tsx
**Purpose:** Renders a dropdown for selecting different chat modes.

**Exported Functions:**
- `ModeSelectorvalue: Mode, onChange: (value: Mode) => void, disabled: boolean, title: string, triggerClassName: string, modeShortcutText: string, customModes: ModeConfig[], customModePrompts: CustomModePrompts, disableSearch: boolean` → `any`

**Exported Types:**
- `interface ModeSelectorProps`: value: Mode, onChange: (value: Mode) => void, disabled?: boolean, title: string, triggerClassName?: string

**Key Imports:** `react`, `fzf`, `lucide-react`, `@roo-code/types`, `@roo/modes`

---

### webview-ui\src\components\chat\ProfileViolationWarning.tsx
**Purpose:** Displays a warning message when a profile violation occurs.

**Key Imports:** `react`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\chat\ProgressIndicator.tsx
**Purpose:** Renders a visual progress indicator using VSCode's progress ring.

**Exported Functions:**
- `ProgressIndicator` → `any`

**Key Imports:** `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\chat\QueuedMessages.tsx
**Purpose:** Displays and manages a queue of messages before they are sent.

**Exported Functions:**
- `QueuedMessagesqueue: QueuedMessage[], onRemove: (index: number) => void, onUpdate: (index: number, newText: string) => void` → `any`

**Exported Types:**
- `interface QueuedMessagesProps`: queue: QueuedMessage[], onRemove: (index: number) => void, onUpdate: (index: number, newText: string) => void

**Key Imports:** `react`, `react-i18next`, `@roo-code/types`, `@src/components/ui`

---

### webview-ui\src\components\chat\ReasoningBlock.tsx
**Purpose:** Renders a block displaying reasoning information with streaming updates.

**Exported Functions:**
- `ReasoningBlockcontent: string, isStreaming: boolean, isLast: boolean` → `any`

**Exported Types:**
- `interface ReasoningBlockProps`: content: string, ts: number, isStreaming: boolean, isLast: boolean, metadata?: any

**Key Imports:** `react`, `react-i18next`, `@src/context/ExtensionStateContext`, `../common/MarkdownBlock`, `lucide-react`

---

### webview-ui\src\components\chat\ShareButton.tsx
**Purpose:** Provides a button to share chat history items with various options.

**Exported Functions:**
- `ShareButtonitem: HistoryItem, disabled: boolean, showLabel: boolean` → `any`

**Exported Types:**
- `interface ShareButtonProps`: item?: HistoryItem, disabled?: boolean, showLabel?: boolean

**Key Imports:** `react`, `react-i18next`, `lucide-react`, `@roo-code/types`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\SlashCommandItem.tsx
**Purpose:** Renders a single slash command item with edit and delete actions.

**Exported Functions:**
- `SlashCommandItemcommand: Command, onDelete: (command: Command) => void, onClick: (command: Command) => void` → `any`

**Exported Types:**
- `interface SlashCommandItemProps`: command: Command, onDelete: (command: Command) => void, onClick?: (command: Command) => void

**Key Imports:** `react`, `lucide-react`, `@roo/ExtensionMessage`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\chat\SlashCommandItemSimple.tsx
**Purpose:** Displays a simplified slash command item within the chat interface.

**Exported Functions:**
- `SlashCommandItemSimplecommand: Command, onClick: (command: Command) => void` → `any`

**Exported Types:**
- `interface SlashCommandItemSimpleProps`: command: Command, onClick?: (command: Command) => void

**Key Imports:** `react`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\chat\SystemPromptWarning.tsx
**Purpose:** Displays a warning message related to system prompts.

**Key Imports:** `react`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\chat\TaskActions.tsx
**Purpose:** Renders action buttons for tasks, including export and copy.

**Exported Functions:**
- `TaskActionsitem: HistoryItem, buttonsDisabled: boolean` → `any`

**Exported Types:**
- `interface TaskActionsProps`: item?: HistoryItem, buttonsDisabled: boolean

**Key Imports:** `react`, `react-i18next`, `@roo-code/types`, `@src/utils/vscode`, `@src/utils/clipboard`

---

### webview-ui\src\components\chat\TaskHeader.tsx
**Purpose:** Displays the header information for a chat task.

**Exported Types:**
- `interface TaskHeaderProps`: task: ClineMessage, tokensIn: number, tokensOut: number, cacheWrites?: number, cacheReads?: number

**Key Imports:** `react`, `react-i18next`, `@src/hooks/useCloudUpsell`, `@src/components/cloud/CloudUpsellDialog`, `@src/components/common/DismissibleUpsell`, `lucide-react`, `pretty-bytes`

---

### webview-ui\src\components\chat\TodoListDisplay.tsx
**Purpose:** Renders a display of a todo list within the chat interface.

**Exported Functions:**
- `TodoListDisplaytodos: any[]` → `any`

**Key Imports:** `react`

---

### webview-ui\src\components\chat\UpdateTodoListToolBlock.tsx
**Purpose:** Provides an editable todo list component with change notifications.

**Exported Types:**
- `interface UpdateTodoListToolBlockProps`: todos?: TodoItem[], content?: string, onChange: (todos: TodoItem[]) => void, editable?: boolean, userEdited?: boolean

**Key Imports:** `react`, `../common/ToolUseBlock`, `../common/MarkdownBlock`

---

### webview-ui\src\components\cloud\__tests__\CloudUpsellDialog.spec.tsx
**Purpose:** Tests the CloudUpsellDialog component's rendering and behavior.

**Key Imports:** `@testing-library/react`, `vitest`, `../CloudUpsellDialog`

---

### webview-ui\src\components\cloud\__tests__\CloudView.spec.tsx
**Purpose:** Tests the CloudView component's rendering and functionality.

**Key Imports:** `@/utils/test-utils`, `../CloudView`

---

### webview-ui\src\components\cloud\CloudAccountSwitcher.tsx
**Purpose:** Provides a UI for switching between cloud accounts and organizations.

**Exported Functions:**
- `CloudAccountSwitcher` → `JSX.Element | null`
- `handleOrganizationChangevalue: string` → `Promise<void>`
- `renderAccountIconorg: CloudOrganizationMembership` → `JSX.Element`

**Key Imports:** `react`, `lucide-react`, `@/components/ui/select`, `@src/i18n/TranslationContext`, `@src/utils/vscode`

---

### webview-ui\src\components\cloud\CloudUpsellDialog.tsx
**Purpose:** Renders a dialog promoting cloud benefits and features.

**Exported Functions:**
- `renderCloudBenefitsContentt: any` → `JSX.Element`
- `CloudUpsellDialogprops: CloudUpsellDialogProps` → `JSX.Element`

**Exported Types:**
- `interface CloudUpsellDialogProps`: open: boolean, onOpenChange: (open: boolean) => void, onConnect: () => void

**Key Imports:** `react-i18next`, `@/components/ui`, `../welcome/RooHero`, `lucide-react`, `@radix-ui/react-dialog`

---

### webview-ui\src\components\cloud\CloudView.tsx
**Purpose:** Manages the cloud view, handling authentication and feature toggles.

**Exported Functions:**
- `CloudViewprops: CloudViewProps` → `JSX.Element`
- `handleConnectClick` → `void`
- `handleManualUrlChangeevent: React.ChangeEvent<HTMLInputElement>` → `void`
- `handleKeyDownevent: React.KeyboardEvent<HTMLInputElement>` → `void`
- `handleShowManualEntry` → `void`
- `handleReset` → `void`
- `handleLogoutClick` → `void`
- `handleVisitCloudWebsite` → `void`
- `handleOpenCloudUrl` → `void`
- `handleRemoteControlToggleenabled: boolean` → `void`
- `handleTaskSyncToggleenabled: boolean` → `void`

**Exported Types:**
- `type CloudViewProps`: userInfo: CloudUserInfo | null, isAuthenticated: boolean, cloudApiUrl?: string, onDone: () => void, organizations?: CloudOrganizationMembership[]

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\cloud\OrganizationSwitcher.tsx
**Purpose:** Provides a UI for switching between organizations in the cloud.

**Exported Functions:**
- `OrganizationSwitcherprops: OrganizationSwitcherProps` → `JSX.Element`
- `handleMessageevent: MessageEvent` → `void`
- `handleOrganizationChangevalue: string` → `Promise<void>`

**Exported Types:**
- `type OrganizationSwitcherProps`: userInfo: CloudUserInfo, organizations: CloudOrganizationMembership[], onOrganizationChange?: (organizationId: string | null) => void, cloudApiUrl?: string

**Key Imports:** `react`, `lucide-react`, `@/components/ui/select`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/utils/vscode`

---

### webview-ui\src\components\common\__mocks__\CodeBlock.tsx
**Purpose:** Provides a mock CodeBlock component for testing purposes.

**Key Imports:** `react`

---

### webview-ui\src\components\common\__mocks__\MarkdownBlock.tsx
**Purpose:** Provides a mock MarkdownBlock component for testing.

**Key Imports:** `react`

---

### webview-ui\src\components\common\__tests__\CodeBlock.spec.tsx
**Purpose:** Tests the CodeBlock component, mocking dependencies for isolated rendering.

**Key Imports:** `vitest`, `../CodeBlock`, `@/utils/test-utils`, `shiki`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\common\__tests__\DismissibleUpsell.spec.tsx
**Purpose:** Tests DismissibleUpsell component, simulating user interactions and API calls.

**Exported Functions:**
- `makeUpsellVisible` → ``

**Key Imports:** `@testing-library/react`, `vitest`, `../DismissibleUpsell`, `@roo-code/types`, `@src/utils/vscode`

---

### webview-ui\src\components\common\__tests__\FormattedTextField.spec.tsx
**Purpose:** Tests FormattedTextField component, validating input formatting and parsing.

**Key Imports:** `@testing-library/react`, `../FormattedTextField`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\common\__tests__\ImageViewer.spec.tsx
**Purpose:** Tests ImageViewer component, rendering images with different URI schemes.

**Key Imports:** `@testing-library/react`, `vitest`, `../ImageViewer`, `@src/utils/vscode`

---

### webview-ui\src\components\common\__tests__\MarkdownBlock.spec.tsx
**Purpose:** Tests MarkdownBlock component, rendering markdown content with links.

**Key Imports:** `@/utils/test-utils`, `../MarkdownBlock`, `@src/utils/vscode`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\common\CodeAccordian.tsx
**Purpose:** Renders a code block with an expandable/collapsible accordian.

**Exported Functions:**
- `CodeAccordianprops: CodeAccordianProps` → `JSX.Element`

**Exported Types:**
- `interface CodeAccordianProps`: path?: string, code?: string, language: string, progressStatus?: ToolProgressStatus, isLoading?: boolean

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/getLanguageFromPath`, `@src/utils/removeLeadingNonAlphanumeric`, `./ToolUseBlock`, `./CodeBlock`

---

### webview-ui\src\components\common\CodeBlock.tsx
**Purpose:** Renders a code block with syntax highlighting and copy functionality.

**Exported Functions:**
- `highlightcode: string, language: string` → `Promise<string | undefined>`
- `handleScrollevent: React.UIEvent<HTMLDivElement, UIEvent>` → `void`
- `handleOuterScrollevent: React.UIEvent<HTMLDivElement, UIEvent>` → `void`
- `handleResize` → `void`
- `getScrollContainerelement: HTMLElement | null` → `HTMLElement | null`
- `animateelement: HTMLElement | null, targetScrollTop: number, duration: number` → `void`
- `handleWheelevent: React.WheelEvent<HTMLDivElement>` → `void`
- `handleMouseDownevent: React.MouseEvent<HTMLDivElement, MouseEvent>` → `void`
- `handleMouseUp` → `void`
- `preprops: any` → `JSX.Element`
- `codeprops: any` → `JSX.Element`
- `lineprops: any` → `JSX.Element`

**Exported Types:**
- `interface WebComponentWithShadowRoot`: shadowRoot: ShadowRoot | null

**Key Imports:** `react`, `styled-components`, `@src/utils/clipboard`, `@src/utils/highlighter`, `shiki`, `hast-util-to-jsx-runtime`, `react/jsx-runtime`, `lucide-react`, `@src/i18n/TranslationContext`, `@/components/ui`

---

### webview-ui\src\components\common\DecoratedVSCodeTextField.tsx
**Purpose:** Enhances VSCodeTextField with custom nodes on either side.

**Exported Functions:**
- `VSCodeTextFieldWithNodesInnerprops: VSCodeTextFieldWithNodesProps, forwardedRef: React.Ref<HTMLInputElement>` → `JSX.Element`

**Exported Types:**
- `interface WebComponentWithShadowRoot`: shadowRoot: ShadowRoot | null
- `interface VSCodeTextFieldWithNodesProps`: leftNodes?: ReactNode[], rightNodes?: ReactNode[]

**Key Imports:** `@/lib/utils`, `@vscode/webview-ui-toolkit/react`, `react`, `react`

---

### webview-ui\src\components\common\DismissibleUpsell.tsx
**Purpose:** Displays dismissible upsell messages within the UI.

**Exported Functions:**
- `DismissIcon` → `JSX.Element`

**Exported Types:**
- `interface DismissibleUpsellProps`: upsellId: string, className?: string, icon?: ReactNode, children: ReactNode, variant?: "default" | "banner"

**Key Imports:** `react`, `@src/utils/vscode`, `@src/i18n/TranslationContext`, `@src/utils/TelemetryClient`, `@roo-code/types`

---

### webview-ui\src\components\common\FormattedTextField.tsx
**Purpose:** Formats and parses text input using a specified formatter.

**Exported Types:**
- `interface InputFormatter`: parse: (input: string) => T | undefined, format: (value: T | undefined) => string, filter?: (input: string) => string
- `interface FormattedTextFieldProps`: value: T | undefined, onValueChange: (value: T | undefined) => void, formatter: InputFormatter<T>

**Key Imports:** `react`, `./DecoratedVSCodeTextField`

---

### webview-ui\src\components\common\IconButton.tsx
**Purpose:** Renders a customizable icon button with various styling options.

**Exported Functions:**
- `IconButtonIconButtonProps` → `any`

**Exported Types:**
- `interface IconButtonProps`: icon: string, onClick?: (e: React.MouseEvent) => void, title?: string, size?: "small" | "medium", variant?: "default" | "transparent"

**Key Imports:** `@/components/ui`

---

### webview-ui\src\components\common\ImageBlock.tsx
**Purpose:** Displays an image using different URI and path formats.

**Exported Functions:**
- `ImageBlockImageBlockProps` → `any`

**Exported Types:**
- `interface ImageBlockProps`: imageUri?: string, imagePath?: string, imageData?: string, path?: string

**Key Imports:** `react`, `./ImageViewer`

---

### webview-ui\src\components\common\ImageViewer.tsx
**Purpose:** Displays and provides controls for viewing and interacting with images.

**Exported Functions:**
- `ImageViewerImageViewerProps` → `any`
- `handleZoome: React.MouseEvent` → `void`
- `handleCopye: React.MouseEvent` → `void`
- `handleSavee: React.MouseEvent` → `void`
- `handleOpenInEditore: React.MouseEvent` → `void`
- `adjustZoomamount: number` → `void`
- `handleMouseEntere: React.MouseEvent` → `void`
- `handleMouseLeavee: React.MouseEvent` → `void`

**Exported Types:**
- `interface ImageViewerProps`: imageUri: string, imagePath?: string, alt?: string, showControls?: boolean, className?: string

**Key Imports:** `react`, `@src/utils/clipboard`, `@src/i18n/TranslationContext`, `@src/utils/vscode`, `./MermaidActionButtons`, `./Modal`, `./TabButton`, `./IconButton`, `./ZoomControls`, `@/components/ui`

---

### webview-ui\src\components\common\MarkdownBlock.tsx
**Purpose:** Renders Markdown content with syntax highlighting and KaTeX support.

**Exported Types:**
- `interface MarkdownBlockProps`: markdown?: string

**Key Imports:** `react`, `react-markdown`, `styled-components`, `unist-util-visit`, `rehype-katex`, `remark-math`, `remark-gfm`, `@src/utils/vscode`, `./CodeBlock`, `./MermaidBlock`

---

### webview-ui\src\components\common\MermaidActionButtons.tsx
**Purpose:** Provides action buttons for Mermaid diagrams, including zoom and copy.

**Exported Types:**
- `interface MermaidActionButtonsProps`: onZoom?: (e: React.MouseEvent) => void, onZoomIn?: () => void, onZoomOut?: () => void, onCopy: (e: React.MouseEvent) => void, onSave?: (e: React.MouseEvent) => void, onViewCode: () => void, onClose?: () => void, copyFeedback: boolean, showZoomControls?: boolean, zoomLevel?: number

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `./IconButton`, `./ZoomControls`, `@/components/ui`

---

### webview-ui\src\components\common\MermaidBlock.tsx
**Purpose:** Renders Mermaid diagrams from code with interactive features.

**Exported Functions:**
- `MermaidBlockMermaidBlockProps` → `any`
- `svgToPngsvgEl: SVGElement` → `Promise<string>`
- `handleClicke: React.MouseEvent` → `void`

**Exported Types:**
- `interface MermaidBlockProps`: code: string, isDarkTheme: boolean, showCopyButton?: boolean, showViewCodeButton?: boolean, showZoomControls?: boolean, onDiagramClick?: (e: React.MouseEvent) => void

**Key Imports:** `react`, `mermaid`, `styled-components`, `@src/utils/useDebounceEffect`, `@src/utils/vscode`, `@src/i18n/TranslationContext`, `@src/utils/clipboard`, `./CodeBlock`, `@/components/common/MermaidButton`

---

### webview-ui\src\components\common\MermaidButton.tsx
**Purpose:** Creates a button to display and interact with Mermaid diagrams.

**Exported Functions:**
- `MermaidButtonMermaidButtonProps` → `any`
- `handleZoome: React.MouseEvent` → `Promise<void>`
- `handleCopye: React.MouseEvent` → `void`
- `handleSavee: React.MouseEvent` → `void`
- `adjustZoomamount: number` → `void`
- `handleMouseEntere: React.MouseEvent` → `void`
- `handleMouseLeavee: React.MouseEvent` → `void`

**Exported Types:**
- `interface MermaidButtonProps`: containerRef: React.RefObject<HTMLDivElement>, code: string, isLoading: boolean, svgToPng: (svgEl: SVGElement) => Promise<string>, children: React.ReactNode

**Key Imports:** `react`, `@src/utils/clipboard`, `@src/i18n/TranslationContext`, `@src/utils/vscode`, `./MermaidActionButtons`, `./Modal`, `./TabButton`, `./IconButton`, `./ZoomControls`, `@/components/ui`

---

### webview-ui\src\components\common\Modal.tsx
**Purpose:** Renders a modal component with backdrop and content.

**Exported Functions:**
- `ModalModalProps` → `any`

**Exported Types:**
- `interface ModalProps`: isOpen: boolean, onClose: () => void, children: React.ReactNode, className?: string

---

### webview-ui\src\components\common\Tab.tsx
**Purpose:** Provides tab components for organizing content within the UI.

**Exported Functions:**
- `TabTabProps` → `any`
- `TabHeaderTabProps` → `any`
- `TabContentTabProps` → `any`
- `TabListHTMLAttributes<HTMLDivElement> & { value: string` → `any`

**Exported Types:**
- `type TabProps`

**Key Imports:** `react`, `@/context/ExtensionStateContext`, `@/lib/utils`

---

### webview-ui\src\components\common\TabButton.tsx
**Purpose:** Renders a button for a tab with styling based on active state.

**Exported Functions:**
- `TabButtonTabButtonProps` → `any`

**Exported Types:**
- `interface TabButtonProps`: icon: string, label: string, isActive: boolean, onClick: () => void

---

### webview-ui\src\components\common\TelemetryBanner.tsx
**Purpose:** Displays a banner to inform users about telemetry settings.

**Exported Functions:**
- `TelemetryBanner` → `any`

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/vscode`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\common\Thumbnails.tsx
**Purpose:** Renders a set of image thumbnails with delete and click actions.

**Exported Functions:**
- `ThumbnailsThumbnailsProps` → `any`
- `handleDeleteindex: number` → `void`
- `handleImageClickimage: string` → `void`

**Exported Types:**
- `interface ThumbnailsProps`: images: string[], style?: React.CSSProperties, setImages?: React.Dispatch<React.SetStateAction<string[]>>, onHeightChange?: (height: number) => void

**Key Imports:** `react`, `react-use`, `@src/utils/vscode`

---

### webview-ui\src\components\common\ToolUseBlock.tsx
**Purpose:** Provides styled blocks for tool use information display.

**Exported Functions:**
- `ToolUseBlockReact.HTMLAttributes<HTMLDivElement>` → `any`
- `ToolUseBlockHeaderReact.HTMLAttributes<HTMLDivElement>` → `any`

**Key Imports:** `@/lib/utils`

---

### webview-ui\src\components\common\VersionIndicator.tsx
**Purpose:** Displays the extension version with a clickable action.

**Exported Functions:**
- `VersionIndicatorVersionIndicatorProps` → `any`

**Exported Types:**
- `interface VersionIndicatorProps`: onClick: () => void, className?: string

**Key Imports:** `react`, `react-i18next`, `@roo/package`

---

### webview-ui\src\components\common\VSCodeButtonLink.tsx
**Purpose:** Creates a VS Code styled button that acts as a link.

**Exported Functions:**
- `VSCodeButtonLinkVSCodeButtonLinkProps` → `any`

**Exported Types:**
- `interface VSCodeButtonLinkProps`: href: string, children: React.ReactNode

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\common\ZoomControls.tsx
**Purpose:** Provides zoom controls with continuous zoom functionality.

**Exported Functions:**
- `ZoomControlsZoomControlsProps` → `any`
- `startContinuousZoomamount: number` → `void`
- `stopContinuousZoom` → `void`

**Exported Types:**
- `interface ZoomControlsProps`: zoomLevel: number, zoomInTitle?: string, zoomOutTitle?: string, useContinuousZoom?: boolean, adjustZoom?: (amount: number) => void, zoomInStep?: number, zoomOutStep?: number, onZoomIn?: () => void, onZoomOut?: () => void

**Key Imports:** `./IconButton`, `react`, `@/components/ui`

---

### webview-ui\src\components\ErrorBoundary.tsx
**Purpose:** Provides an error boundary component to catch and report errors.

**Exported Functions:**
- `getDerivedStateFromErrorerror: unknown` → `any`
- `componentDidCatcherror: Error, errorInfo: React.ErrorInfo` → `void`
- `render` → `any`

**Exported Types:**
- `type ErrorProps`: children: React.ReactNode
- `type ErrorState`: error?: string, componentStack?: string | null, timestamp?: number
- `class ErrorBoundary`: constructor, getDerivedStateFromError, componentDidCatch, render

**Key Imports:** `react`, `@src/utils/TelemetryClient`, `react-i18next`, `@src/utils/sourceMapUtils`

---

### webview-ui\src\components\history\__tests__\BatchDeleteTaskDialog.spec.tsx
**Purpose:** Tests the BatchDeleteTaskDialog component's rendering and behavior.

**Key Imports:** `@`, `@/utils/test-utils`, `@/utils/vscode`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\history\__tests__\CopyButton.spec.tsx
**Purpose:** Tests the CopyButton component's functionality for copying task content.

**Key Imports:** `@/utils/test-utils`, `@/components/ui/hooks`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\history\__tests__\DeleteButton.spec.tsx
**Purpose:** Tests the DeleteButton component's click event and delete action.

**Key Imports:** `@/utils/test-utils`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\history\__tests__\DeleteTaskDialog.spec.tsx
**Purpose:** Tests the DeleteTaskDialog component's rendering and delete functionality.

**Key Imports:** `@/utils/test-utils`, `@/utils/vscode`, `@/i18n/TranslationContext`, `react-use`

---

### webview-ui\src\components\history\__tests__\ExportButton.spec.tsx
**Purpose:** Tests the ExportButton component's message sending on click.

**Key Imports:** `@/utils/test-utils`, `@src/utils/vscode`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\history\__tests__\HistoryPreview.spec.tsx
**Purpose:** Tests the HistoryPreview component's rendering of task items.

**Key Imports:** `@/utils/test-utils`, `@roo-code/types`, `../useTaskSearch`, `../TaskItem`

---

### webview-ui\src\components\history\__tests__\HistoryView.spec.tsx
**Purpose:** Tests the HistoryView component's rendering and button click actions.

**Key Imports:** `@/utils/test-utils`, `@src/context/ExtensionStateContext`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\history\__tests__\TaskItem.spec.tsx
**Purpose:** Tests the TaskItem component's rendering and selection handling.

**Key Imports:** `@/utils/test-utils`, `@src/i18n/TranslationContext`, `@/utils/format`

---

### webview-ui\src\components\history\__tests__\TaskItemFooter.spec.tsx
**Purpose:** Tests the TaskItemFooter component's rendering of information.

**Key Imports:** `@/utils/test-utils`, `@src/i18n/TranslationContext`, `@/utils/format`

---

### webview-ui\src\components\history\__tests__\useTaskSearch.spec.tsx
**Purpose:** Tests the useTaskSearch hook's filtering and search functionality.

**Key Imports:** `@/utils/test-utils`, `@roo-code/types`, `@/context/ExtensionStateContext`, `@/utils/highlight`

---

### webview-ui\src\components\history\BatchDeleteTaskDialog.tsx
**Purpose:** Displays a dialog for batch deletion of selected tasks.

**Exported Functions:**
- `BatchDeleteTaskDialogprops: BatchDeleteTaskDialogProps` → `any`

**Exported Types:**
- `interface BatchDeleteTaskDialogProps`: taskIds: string[]

**Key Imports:** `react`, `@/i18n/TranslationContext`, `@/components/ui`, `@/utils/vscode`, `@radix-ui/react-alert-dialog`

---

### webview-ui\src\components\history\CopyButton.tsx
**Purpose:** Renders a button to copy the task content to the clipboard.

**Exported Functions:**
- `CopyButtonprops: CopyButtonProps` → `any`

**Exported Types:**
- `type CopyButtonProps`: itemTask: string

**Key Imports:** `react`, `@/components/ui/hooks`, `@/components/ui`, `@/i18n/TranslationContext`, `@/lib/utils`

---

### webview-ui\src\components\history\DeleteButton.tsx
**Purpose:** Renders a button to delete a specific task item.

**Exported Functions:**
- `DeleteButtonprops: DeleteButtonProps` → `any`

**Exported Types:**
- `type DeleteButtonProps`: itemId: string, onDelete?: (taskId: string) => void

**Key Imports:** `react`, `@/components/ui`, `@/i18n/TranslationContext`, `@/utils/vscode`

---

### webview-ui\src\components\history\DeleteTaskDialog.tsx
**Purpose:** Displays a dialog to confirm the deletion of a task.

**Exported Functions:**
- `DeleteTaskDialogprops: DeleteTaskDialogProps` → `any`

**Exported Types:**
- `interface DeleteTaskDialogProps`: taskId: string

**Key Imports:** `react`, `react-use`, `@radix-ui/react-alert-dialog`, `@/components/ui`, `@/i18n/TranslationContext`, `@/utils/vscode`

---

### webview-ui\src\components\history\ExportButton.tsx
**Purpose:** Renders a button to export a specific task item.

**Exported Functions:**
- `ExportButtonprops: { itemId: string }` → `any`

**Key Imports:** `@/utils/vscode`, `@/components/ui`, `@/i18n/TranslationContext`, `react`

---

### webview-ui\src\components\history\HistoryPreview.tsx
**Purpose:** Displays a preview of recent tasks with a link to view all history.

**Exported Functions:**
- `handleViewAllHistory` → `void`

**Key Imports:** `react`, `@src/utils/vscode`, `@src/i18n/TranslationContext`, `./useTaskSearch`, `./TaskItem`

---

### webview-ui\src\components\history\HistoryView.tsx
**Purpose:** Renders the history view, displaying tasks with search and sort options.

**Exported Functions:**
- `HistoryViewprops: HistoryViewProps` → `any`
- `toggleSelectionMode` → `void`
- `toggleTaskSelection` → `void`
- `toggleSelectAll` → `void`
- `handleBatchDelete` → `void`

**Exported Types:**
- `type HistoryViewProps`: onDone: () => void
- `type SortOption`

**Key Imports:** `react`, `./DeleteTaskDialog`, `./BatchDeleteTaskDialog`, `react-virtuoso`, `@vscode/webview-ui-toolkit/react`, `@/components/ui`, `@/i18n/TranslationContext`, `../common/Tab`, `./useTaskSearch`

---

### webview-ui\src\components\history\TaskItem.tsx
**Purpose:** Renders a single task item with different display variants.

**Exported Functions:**
- `TaskItemprops: TaskItemProps` → `any`
- `handleClick` → `void`

**Exported Types:**
- `interface DisplayHistoryItem`: highlight?: string
- `interface TaskItemProps`: item: DisplayHistoryItem, variant: "compact" | "full", showWorkspace?: boolean, isSelectionMode?: boolean, isSelected?: boolean, onToggleSelection?: (taskId: string, isSelected: boolean) => void, onDelete?: (taskId: string) => void, className?: string

**Key Imports:** `react`, `@roo-code/types`, `@/utils/vscode`, `@/lib/utils`, `@/components/ui/checkbox`, `./TaskItemFooter`

---

### webview-ui\src\components\history\TaskItemFooter.tsx
**Purpose:** Renders the footer for a task item, displaying metadata and actions.

**Exported Types:**
- `interface TaskItemFooterProps`: item: HistoryItem, variant: "compact" | "full", isSelectionMode?: boolean, onDelete?: (taskId: string) => void

**Key Imports:** `react`, `@roo-code/types`, `@/utils/format`, `./CopyButton`, `./ExportButton`, `./DeleteButton`, `../ui/standard-tooltip`

---

### webview-ui\src\components\history\useTaskSearch.ts
**Purpose:** Provides search and sort functionality for task history.

**Exported Functions:**
- `useTaskSearch` → `any`

**Exported Types:**
- `type SortOption`

**Key Imports:** `react`, `fzf`, `@/utils/highlight`, `@/context/ExtensionStateContext`

---

### webview-ui\src\components\human-relay\HumanRelayDialog.tsx
**Purpose:** Displays a dialog for human relay, handling copy and submission.

**Exported Functions:**
- `handleCopy` → ``
- `handleSubmite: React.FormEvent<HTMLFormElement>` → ``
- `handleCancel` → ``

**Exported Types:**
- `interface HumanRelayDialogProps`: isOpen, onClose, requestId, promptText, onSubmit, onCancel

**Key Imports:** `react`, `../ui/button`, `../ui/dialog`, `../ui/textarea`, `../ui/hooks`, `lucide-react`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\marketplace\__tests__\MarketplaceListView.spec.tsx
**Functions:** `renderWithProviders`

---

### webview-ui\src\components\marketplace\__tests__\MarketplaceView.spec.tsx
---

### webview-ui\src\components\marketplace\__tests__\MarketplaceViewStateManager.spec.ts
---

### webview-ui\src\components\marketplace\components\__tests__\MarketplaceInstallModal-optional-params.spec.tsx
**Purpose:** Tests the MarketplaceInstallModal with optional parameters.

**Key Imports:** `@/utils/test-utils`, `@roo-code/types`, `../MarketplaceInstallModal`, `@/utils/vscode`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\marketplace\components\__tests__\MarketplaceInstallModal.spec.tsx
**Purpose:** Tests the MarketplaceInstallModal component's installation process.

**Key Imports:** `@/utils/test-utils`, `@roo-code/types`, `../MarketplaceInstallModal`, `@/utils/vscode`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\marketplace\components\__tests__\MarketplaceItemCard.spec.tsx
**Purpose:** Tests the MarketplaceItemCard component's rendering and interactions.

**Key Imports:** `@/utils/test-utils`, `@testing-library/user-event`, `@roo-code/types`, `@/utils/vscode`, `@/components/ui/tooltip`, `../MarketplaceItemCard`

---

### webview-ui\src\components\marketplace\components\MarketplaceInstallModal.tsx
**Purpose:** Provides a modal for installing marketplace items with configurations.

**Exported Functions:**
- `handleMessageevent: MessageEvent<{ type: string; payload?: any }>` → ``
- `handleInstall` → ``
- `handlePostInstallAction` → ``

**Exported Types:**
- `interface MarketplaceInstallModalProps`: item, isOpen, onClose, hasWorkspace

**Key Imports:** `react`, `@roo-code/types`, `@/utils/vscode`, `@/i18n/TranslationContext`, `@/components/ui/dialog`, `@/components/ui/button`

---

### webview-ui\src\components\marketplace\components\MarketplaceItemCard.tsx
**Purpose:** Renders a card displaying marketplace item information and actions.

**Exported Functions:**
- `handleMessageevent: MessageEvent<{ type: string; payload?: any }>` → ``
- `handleInstallClick` → ``
- `handleOpenAuthorUrl` → ``

**Exported Types:**
- `interface ItemInstalledMetadata`: type
- `interface MarketplaceItemCardProps`: item, filters, setFilters, installed

**Key Imports:** `react`, `@roo-code/types`, `@/utils/vscode`, `@/utils/TelemetryClient`, `../MarketplaceViewStateManager`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\marketplace\IssueFooter.tsx
**Purpose:** Renders a footer with a link to open a GitHub issue.

**Exported Functions:**
- `IssueFooter` → `React.FC`

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\marketplace\MarketplaceListView.tsx
**Purpose:** Displays a list of marketplace items with filtering and sorting options.

**Exported Functions:**
- `MarketplaceListViewstateManager: MarketplaceViewStateManager, allTags: string[], filteredTags: string[], filterByType?: "mcp" | "mode"` → `any`

**Exported Types:**
- `interface MarketplaceListViewProps`: stateManager: MarketplaceViewStateManager, allTags: string[], filteredTags: string[], filterByType?: "mcp" | "mode"

**Key Imports:** `react`, `@/components/ui/input`, `@/components/ui/button`, `@/components/ui/select`, `./components/MarketplaceItemCard`

---

### webview-ui\src\components\marketplace\MarketplaceView.tsx
**Purpose:** Manages and renders the main marketplace view with tabs and content.

**Exported Functions:**
- `MarketplaceViewstateManager: MarketplaceViewStateManager, onDone, targetTab` → `any`

**Exported Types:**
- `interface MarketplaceViewProps`: onDone?: () => void, stateManager: MarketplaceViewStateManager, targetTab?: "mcp" | "mode"

**Key Imports:** `react`, `@/components/ui/button`, `../common/Tab`, `./MarketplaceViewStateManager`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\marketplace\MarketplaceViewStateManager.ts
**Purpose:** Manages the state for the marketplace view and handles transitions.

**Exported Types:**
- `interface ViewState`: allItems: MarketplaceItem[], organizationMcps: MarketplaceItem[], displayItems?: MarketplaceItem[], isFetching: boolean

**Key Imports:** `MarketplaceItem`, `../../utils/vscode`, `../../../../src/shared/WebviewMessage`, `../../../../src/shared/ExtensionMessage`

---

### webview-ui\src\components\marketplace\useStateManager.ts
**Purpose:** Provides a state management hook for the marketplace view.

**Exported Functions:**
- `useStateManagerexistingManager?: MarketplaceViewStateManager` → `any`

**Key Imports:** `react`, `./MarketplaceViewStateManager`

---

### webview-ui\src\components\mcp\__tests__\McpToolRow.spec.tsx
**Functions:** `MockVSCodeCheckbox`

---

### webview-ui\src\components\mcp\McpEnabledToggle.tsx
**Purpose:** Renders a toggle to enable or disable MCP functionality.

**Exported Functions:**
- `McpEnabledToggle` → `any`

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `react`, `@src/context/ExtensionStateContext`, `@src/i18n/TranslationContext`, `@src/utils/vscode`

---

### webview-ui\src\components\mcp\McpErrorRow.tsx
**Purpose:** Displays a single MCP error entry with details and formatting.

**Exported Functions:**
- `McpErrorRowerror: McpErrorEntry` → `any`

**Key Imports:** `react`, `date-fns`, `@roo/mcp`

---

### webview-ui\src\components\mcp\McpResourceRow.tsx
**Purpose:** Renders a row displaying information about an MCP resource.

**Exported Functions:**
- `McpResourceRowitem: McpResource | McpResourceTemplate` → `any`

**Key Imports:** `McpResource`, `McpResourceTemplate`

---

### webview-ui\src\components\mcp\McpToolRow.tsx
**Purpose:** Renders a row for an MCP tool with controls and information.

**Exported Functions:**
- `McpToolRowtool, serverName, serverSource, alwaysAllowMcp, isInChatContext` → `any`
- `handleAlwaysAllowChange` → `any`
- `handleEnabledForPromptChange` → `any`

**Exported Types:**
- `type McpToolRowProps`: tool: McpTool, serverName?: string, serverSource?: "global" | "project", alwaysAllowMcp?: boolean

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `McpTool`, `@src/i18n/TranslationContext`, `@src/utils/vscode`, `@/components/ui`

---

### webview-ui\src\components\mcp\McpView.tsx
**Purpose:** Displays and manages the MCP configuration and server status.

**Exported Functions:**
- `McpViewonDone: () => void` → `any`
- `ServerRow` → `any`
- `getStatusColor` → `any`
- `handleRowClick` → `any`
- `handleRestart` → `any`
- `handleTimeoutChange` → `any`
- `handleDelete` → `any`

**Exported Types:**
- `type McpViewProps`: onDone: () => void

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo/mcp`, `@src/utils/vscode`

---

### webview-ui\src\components\modes\__tests__\ModesView.spec.tsx
**Purpose:** Tests the rendering and behavior of the ModesView component.

**Exported Functions:**
- `renderPromptsViewprops = {}` → `any`

**Key Imports:** `render`, `screen`, `fireEvent`, `waitFor`, `@`

---

### webview-ui\src\components\modes\DeleteModeDialog.tsx
**Purpose:** Provides a dialog for deleting a mode with confirmation.

**Exported Types:**
- `interface DeleteModeDialogProps`: open: boolean, onOpenChange: (open: boolean) => void, modeToDelete: { slug: string, name: string, source?: string, rulesFolderPath?: string } | null, onConfirm: () => void

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\modes\ModesView.tsx
**Purpose:** Renders the Modes view, allowing mode management and configuration.

**Exported Functions:**
- `getGroupName` → `any`
- `ModesView` → `any`
- `handleClickOutside` → `any`
- `handler` → `any`
- `handleAgentReset` → `any`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `react-i18next`, `lucide-react`, `@roo-code/types`, `@roo/modes`

---

### webview-ui\src\components\settings\__tests__\ApiConfigManager.spec.tsx
**Functions:** `getRenameForm`, `getDialogContent`

---

### webview-ui\src\components\settings\__tests__\ApiOptions.provider-filtering.spec.tsx
**Functions:** `renderWithProviders`

---

### webview-ui\src\components\settings\__tests__\ApiOptions.spec.tsx
**Functions:** `renderApiOptions`

---

### webview-ui\src\components\settings\__tests__\AutoApproveToggle.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ContextManagementSettings.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ImageGenerationSettings.spec.tsx
---

### webview-ui\src\components\settings\__tests__\MaxCostInput.spec.tsx
---

### webview-ui\src\components\settings\__tests__\MaxRequestsInput.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ModelPicker.deprecated.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ModelPicker.spec.tsx
**Purpose:** Tests the ModelPicker component for settings configuration.

**Exported Functions:**
- `renderModelPicker` → ``

**Exported Types:**
- `interface ModelInfo`: maxTokens, contextWindow, supportsImages, inputPrice, outputPrice

**Key Imports:** `@`, `@roo-code/types`, `react`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\settings\__tests__\SettingsView.change-detection.spec.tsx
**Purpose:** Tests SettingsView component's change detection behavior.

**Key Imports:** `@testing-library/react`, `vitest`, `@tanstack/react-query`, `react`, `@src/context/ExtensionStateContext`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\__tests__\SettingsView.spec.tsx
**Purpose:** Tests the SettingsView component's rendering and interactions.

**Key Imports:** `@testing-library/react`, `@tanstack/react-query`, `@/utils/vscode`, `@/context/ExtensionStateContext`, `../ApiConfigManager`

---

### webview-ui\src\components\settings\__tests__\SettingsView.unsaved-changes.spec.tsx
**Purpose:** Tests SettingsView component's handling of unsaved changes.

**Key Imports:** `@testing-library/react`, `vitest`, `@tanstack/react-query`, `react`, `@src/context/ExtensionStateContext`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\__tests__\SlashCommandsSettings.spec.tsx
**Purpose:** Tests the SlashCommandsSettings component's functionality.

**Key Imports:** `@testing-library/react`, `@roo/ExtensionMessage`, `@/context/ExtensionStateContext`, `@/utils/vscode`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\settings\__tests__\TemperatureControl.spec.tsx
**Purpose:** Tests the TemperatureControl component's rendering and behavior.

**Key Imports:** `@testing-library/react`, `../TemperatureControl`, `@/components/ui`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\settings\__tests__\ThinkingBudget.spec.tsx
**Purpose:** Tests the ThinkingBudget component's functionality.

**Key Imports:** `@testing-library/react`, `@roo-code/types`, `../ThinkingBudget`, `@/components/ui`, `@/components/ui/hooks/useSelectedModel`

---

### webview-ui\src\components\settings\__tests__\TodoListSettingsControl.spec.tsx
**Purpose:** Tests the TodoListSettingsControl component's rendering.

**Key Imports:** `@testing-library/react`, `../TodoListSettingsControl`, `@/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\settings\__tests__\UISettings.spec.tsx
**Purpose:** Tests the UISettings component's rendering and interactions.

**Key Imports:** `@testing-library/react`, `vitest`, `../UISettings`

---

### webview-ui\src\components\settings\About.tsx
**Purpose:** Renders the About section within the settings, displaying version and telemetry options.

**Exported Types:**
- `type AboutProps`: telemetrySetting, setTelemetrySetting, className, ...props

**Key Imports:** `react`, `useAppTranslation`, `Trans`, `Info`, `VSCodeCheckbox`

---

### webview-ui\src\components\settings\ApiConfigManager.tsx
**Purpose:** Manages API configuration profiles, allowing creation, renaming, and deletion.

**Exported Functions:**
- `ApiConfigManager{
	currentApiConfigName = "",
	listApiConfigMeta = [],
	organizationAllowList,
	onSelectConfig,
	onDeleteConfig,
	onRenameConfig,
	onUpsertConfig,
}` → `any`
- `resetCreateState` → `any`
- `resetRenameState` → `any`
- `handleSelectConfigconfigName: string` → `void`
- `handleAdd` → `void`
- `handleStartRenameconfigName: string` → `void`
- `handleCancel` → `void`
- `handleSave` → `void`
- `handleNewProfileSave` → `void`
- `handleDeleteconfigName: string` → `void`

**Exported Types:**
- `interface ApiConfigManagerProps`: currentApiConfigName?, listApiConfigMeta?, organizationAllowList?, onSelectConfig, onDeleteConfig

**Key Imports:** `memo`, `useEffect`, `useRef`, `useState`, `VSCodeTextField`

---

### webview-ui\src\components\settings\ApiErrorMessage.tsx
**Purpose:** Displays API error messages with a close icon and optional children.

**Exported Types:**
- `interface ApiErrorMessageProps`: errorMessage, children?

**Key Imports:** `React`

---

### webview-ui\src\components\settings\ApiOptions.tsx
**Purpose:** Renders and manages API options, including model selection and configuration.

**Exported Functions:**
- `ApiOptions` → `any`
- `validateAndResetModelproviderName: ProviderName` → `void`

**Key Imports:** `React`, `memo`, `useCallback`, `useEffect`, `useMemo`

---

### webview-ui\src\components\settings\AutoApproveSettings.tsx
**Purpose:** Provides settings for auto-approval of code actions, with various toggle options.

**Exported Types:**
- `type AutoApproveSettingsProps`: alwaysAllowReadOnly?, alwaysAllowReadOnlyOutsideWorkspace?, alwaysAllowWrite?, alwaysAllowWriteOutsideWorkspace?, alwaysAllowWriteProtected?

**Key Imports:** `HTMLAttributes`, `useState`, `X`, `CheckCheck`, `Trans`

---

### webview-ui\src\components\settings\AutoApproveToggle.tsx
**Purpose:** Defines and renders individual auto-approve toggle settings within the UI.

**Exported Types:**
- `type AutoApproveSetting`
- `type AutoApproveConfig`: key, labelKey, descriptionKey, icon, testId
- `type AutoApproveToggles`

**Exported Constants:**
- `autoApproveSettingsConfig` = `{}`

**Key Imports:** `type`, `GlobalSettings`, `useAppTranslation`, `cn`, `Button`

---

### webview-ui\src\components\settings\BrowserSettings.tsx
**Purpose:** Manages browser-related settings, including tool enabling and remote configuration.

**Exported Types:**
- `type BrowserSettingsProps`: browserToolEnabled?, browserViewportSize?, screenshotQuality?, remoteBrowserHost?, remoteBrowserEnabled?

**Key Imports:** `VSCodeButton`, `VSCodeCheckbox`, `VSCodeTextField`, `VSCodeLink`, `SquareMousePointer`

---

### webview-ui\src\components\settings\CheckpointSettings.tsx
**Purpose:** Provides settings related to checkpoint functionality within the application.

**Exported Types:**
- `type CheckpointSettingsProps`: enableCheckpoints?, setCachedStateField

**Key Imports:** `HTMLAttributes`, `useAppTranslation`, `VSCodeCheckbox`, `VSCodeLink`, `GitBranch`

---

### webview-ui\src\components\settings\ConsecutiveMistakeLimitControl.tsx
**Purpose:** Renders a slider control for setting the consecutive mistake limit.

**Exported Types:**
- `interface ConsecutiveMistakeLimitControlProps`: value, onChange

**Key Imports:** `React`, `useCallback`, `Slider`, `useAppTranslation`

---

### webview-ui\src\components\settings\constants.ts
**Purpose:** Defines constants for providers and models used in settings.

**Exported Constants:**
- `MODELS_BY_PROVIDER` = `{}`
- `PROVIDERS` = `[]`

**Key Imports:** `type`, `ProviderName`, `ModelInfo`, `anthropicModels`, `bedrockModels`

---

### webview-ui\src\components\settings\ContextManagementSettings.tsx
**Purpose:** Manages context settings, including auto-condensation and file limits.

**Exported Types:**
- `type ContextManagementSettingsProps`: autoCondenseContext, autoCondenseContextPercent, listApiConfigMeta, maxOpenTabsContext, maxWorkspaceFiles

**Key Imports:** `HTMLAttributes`, `React`, `useAppTranslation`, `VSCodeCheckbox`, `Database`

---

### webview-ui\src\components\settings\DiffSettingsControl.tsx
**Purpose:** Provides controls for enabling and configuring diff settings.

**Exported Types:**
- `interface DiffSettingsControlProps`: diffEnabled?, fuzzyMatchThreshold?, onChange

**Key Imports:** `React`, `useCallback`, `Slider`, `useAppTranslation`

---

### webview-ui\src\components\settings\ExperimentalFeature.tsx
**Purpose:** Renders an experimental feature toggle with a description.

**Exported Types:**
- `interface ExperimentalFeatureProps`: enabled, onChange, experimentKey?

**Key Imports:** `VSCodeCheckbox`, `useAppTranslation`

---

### webview-ui\src\components\settings\ExperimentalSettings.tsx
**Purpose:** Renders experimental settings, including feature toggles and configurations.

**Exported Types:**
- `type ExperimentalSettingsProps`: experiments, setExperimentEnabled, apiConfiguration, setApiConfigurationField, openRouterImageApiKey

**Key Imports:** `HTMLAttributes`, `FlaskConical`, `type`, `Experiments`, `EXPERIMENT_IDS`

---

### webview-ui\src\components\settings\ImageGenerationSettings.tsx
**Purpose:** Renders image generation settings with model and API key inputs.

**Exported Functions:**
- `ImageGenerationSettingsImageGenerationSettingsProps` → `any`
- `handleApiKeyChange` → ``
- `handleModelChange` → ``

**Exported Types:**
- `interface ImageGenerationSettingsProps`: enabled: boolean, onChange: (enabled: boolean) => void, openRouterImageApiKey?: string, openRouterImageGenerationSelectedModel?: string, setOpenRouterImageApiKey: (apiKey: string) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@/i18n/TranslationContext`, `useState`, `useEffect`

---

### webview-ui\src\components\settings\LanguageSettings.tsx
**Purpose:** Provides language selection settings using a dropdown component.

**Exported Functions:**
- `LanguageSettingsLanguageSettingsProps` → `any`

**Exported Types:**
- `type LanguageSettingsProps`: language: string, setCachedStateField: SetCachedStateField<"language">, className?: string, ...props: HTMLAttributes<HTMLDivElement>

**Key Imports:** `react`, `@roo-code/types`, `@roo/language`, `@src/lib/utils`, `@src/components/ui`

---

### webview-ui\src\components\settings\MaxCostInput.tsx
**Purpose:** Renders an input field for setting the maximum API cost limit.

**Exported Functions:**
- `MaxCostInputMaxCostInputProps` → `any`

**Exported Types:**
- `interface MaxCostInputProps`: allowedMaxCost?: number, onValueChange: (value: number | undefined) => void

**Key Imports:** `react-i18next`, `@/utils/vscode`, `react`, `FormattedTextField`, `unlimitedDecimalFormatter`

---

### webview-ui\src\components\settings\MaxLimitInputs.tsx
**Purpose:** Displays inputs for maximum request and cost limits.

**Exported Functions:**
- `MaxLimitInputsMaxLimitInputsProps` → `React.FC<MaxLimitInputsProps>`

**Exported Types:**
- `interface MaxLimitInputsProps`: allowedMaxRequests?: number, allowedMaxCost?: number, onMaxRequestsChange: (value: number | undefined) => void, onMaxCostChange: (value: number | undefined) => void

**Key Imports:** `react-i18next`, `MaxRequestsInput`, `MaxCostInput`, `React`

---

### webview-ui\src\components\settings\MaxRequestsInput.tsx
**Purpose:** Renders an input field for setting the maximum API request limit.

**Exported Functions:**
- `MaxRequestsInputMaxRequestsInputProps` → `any`

**Exported Types:**
- `interface MaxRequestsInputProps`: allowedMaxRequests?: number, onValueChange: (value: number | undefined) => void

**Key Imports:** `react-i18next`, `@/utils/vscode`, `react`, `FormattedTextField`, `unlimitedIntegerFormatter`

---

### webview-ui\src\components\settings\ModelDescriptionMarkdown.tsx
**Purpose:** Displays a markdown description with expand/collapse functionality.

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `react`, `react-remark`, `@/lib/utils`, `@/components/ui`

---

### webview-ui\src\components\settings\ModelInfoView.tsx
**Purpose:** Renders detailed information about a selected model.

**Exported Functions:**
- `ModelInfoViewModelInfoViewProps` → `any`
- `fmtn?: number` → `any`
- `ModelInfoSupportsItem` → ``

**Exported Types:**
- `type ModelInfoViewProps`: apiProvider?: string, selectedModelId: string, modelInfo?: ModelInfo, isDescriptionExpanded: boolean

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/formatPrice`, `@src/lib/utils`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\ModelPicker.tsx
**Purpose:** Provides a dropdown for selecting a model from available options.

**Exported Functions:**
- `ModelPickerModelPickerProps` → `any`

**Exported Types:**
- `type ModelIdKey`: glamaModelId, openRouterModelId, unboundModelId, requestyModelId
- `interface ModelPickerProps`: defaultModelId: string, models: Record<string, ModelInfo> | null, modelIdKey: ModelIdKey, serviceName: string

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `react-i18next`, `lucide-react`, `@roo-code/types`

---

### webview-ui\src\components\settings\NotificationSettings.tsx
**Purpose:** Renders notification settings including TTS and sound options.

**Exported Functions:**
- `NotificationSettingsNotificationSettingsProps` → `any`

**Exported Types:**
- `type NotificationSettingsProps`: ttsEnabled?: boolean, ttsSpeed?: number, soundEnabled?: boolean, soundVolume?: number, setCachedStateField: SetCachedStateField<"ttsEnabled" | "ttsSpeed" | "soundEnabled" | "soundVolume">

**Key Imports:** `react`, `@/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`, `lucide-react`, `SetCachedStateField`

---

### webview-ui\src\components\settings\PromptsSettings.tsx
**Purpose:** Manages settings related to custom prompts and enhancements.

**Exported Functions:**
- `PromptsSettingsPromptsSettingsProps` → `any`
- `handler` → ``
- `updateSupportPrompt` → ``
- `handleSupportReset` → ``
- `handleTestEnhancement` → ``

**Exported Types:**
- `interface PromptsSettingsProps`: customSupportPrompts: Record<string, string | undefined>, setCustomSupportPrompts: (prompts: Record<string, string | undefined>) => void, includeTaskHistoryInEnhance?: boolean, setIncludeTaskHistoryInEnhance?: (value: boolean) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo/support-prompt`, `@src/utils/vscode`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\__tests__\Bedrock.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\Gemini.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\HuggingFace.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\OpenAICompatible.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\Vertex.spec.tsx
---

### webview-ui\src\components\settings\providers\Anthropic.tsx
**Purpose:** Renders Anthropic-specific API configuration settings.

**Exported Functions:**
- `AnthropicAnthropicProps` → `any`

**Exported Types:**
- `type AnthropicProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Bedrock.tsx
**Purpose:** Renders Bedrock-specific API configuration settings.

**Exported Functions:**
- `BedrockBedrockProps` → `any`

**Exported Types:**
- `type BedrockProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, selectedModelInfo?: ModelInfo

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\BedrockCustomArn.tsx
**Purpose:** Provides a custom ARN input field for Bedrock configuration.

**Exported Functions:**
- `BedrockCustomArnBedrockCustomArnProps` → `any`

**Exported Types:**
- `type BedrockCustomArnProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/validate`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Cerebras.tsx
**Purpose:** Renders Cerebras-specific API configuration settings.

**Exported Functions:**
- `CerebrasCerebrasProps` → `any`

**Exported Types:**
- `type CerebrasProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Chutes.tsx
**Purpose:** Renders Chutes-specific API configuration settings.

**Exported Functions:**
- `ChutesChutesProps` → `any`

**Exported Types:**
- `type ChutesProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\ClaudeCode.tsx
**Purpose:** Renders Claude Code provider settings input fields and descriptions.

**Exported Functions:**
- `handleInputChange(e: Event | React.FormEvent<HTMLElement>)` → `void`

**Exported Types:**
- `interface ClaudeCodeProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\DeepInfra.tsx
**Purpose:** Provides DeepInfra settings input fields and model selection components.

**Exported Functions:**
- `DeepInfra({
	apiConfiguration,
	setApiConfigurationField,
	routerModels,
	refetchRouterModels,
	organizationAllowList,
	modelValidationError,
}: DeepInfraProps)` → `any`

**Exported Types:**
- `type DeepInfraProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, refetchRouterModels: () => void, organizationAllowList: OrganizationAllowList

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/utils/vscode`

---

### webview-ui\src\components\settings\providers\DeepSeek.tsx
**Purpose:** Renders DeepSeek API key input field for provider settings.

**Exported Functions:**
- `DeepSeek({ apiConfiguration, setApiConfigurationField }: DeepSeekProps)` → `any`

**Exported Types:**
- `type DeepSeekProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Doubao.tsx
**Purpose:** Renders Doubao API key input field for provider settings.

**Exported Functions:**
- `Doubao({ apiConfiguration, setApiConfigurationField }: DoubaoProps)` → `any`

**Exported Types:**
- `type DoubaoProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Featherless.tsx
**Purpose:** Renders Featherless API key input field for provider settings.

**Exported Functions:**
- `Featherless({ apiConfiguration, setApiConfigurationField }: FeatherlessProps)` → `any`

**Exported Types:**
- `type FeatherlessProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Fireworks.tsx
**Purpose:** Renders Fireworks API key input field for provider settings.

**Exported Functions:**
- `Fireworks({ apiConfiguration, setApiConfigurationField }: FireworksProps)` → `any`

**Exported Types:**
- `type FireworksProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Gemini.tsx
**Purpose:** Renders Gemini API key input and base URL selection for settings.

**Exported Functions:**
- `Gemini({ apiConfiguration, setApiConfigurationField, fromWelcomeView }: GeminiProps)` → `any`

**Exported Types:**
- `type GeminiProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, fromWelcomeView?: boolean

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Glama.tsx
**Purpose:** Renders Glama API key input and model selection for settings.

**Exported Functions:**
- `Glama({ apiConfiguration, setApiConfigurationField, routerModels, uriScheme, organizationAllowList, modelValidationError }: GlamaProps)` → `any`

**Exported Types:**
- `type GlamaProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, uriScheme?: string, organizationAllowList: OrganizationAllowList

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Groq.tsx
**Purpose:** Renders Groq API key input field for provider settings.

**Exported Functions:**
- `Groq({ apiConfiguration, setApiConfigurationField }: GroqProps)` → `any`

**Exported Types:**
- `type GroqProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\HuggingFace.tsx
**Purpose:** Provides Hugging Face settings, including API key and model selection.

**Exported Functions:**
- `HuggingFace({ apiConfiguration, setApiConfigurationField }: HuggingFaceProps)` → `any`
- `handleModelSelect(option: SearchableSelectOption<HuggingFaceModel> | undefined)` → `void`
- `handleProviderSelect(option: SearchableSelectOption<string> | undefined)` → `void`
- `formatProviderName(provider: string)` → `string`

**Exported Types:**
- `type HuggingFaceModel`: id: string, object: string, created: number, owned_by: string
- `type HuggingFaceProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings], isUserAction?: boolean) => void

**Key Imports:** `react`, `react-use`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\settings\providers\index.ts
**Purpose:** Exports all provider components for settings configuration.

---

### webview-ui\src\components\settings\providers\IOIntelligence.tsx
**Purpose:** Renders IO Intelligence API key and model selection settings.

**Exported Functions:**
- `IOIntelligence({ apiConfiguration, setApiConfigurationField, organizationAllowList, modelValidationError }: IOIntelligenceProps)` → `any`

**Exported Types:**
- `type IOIntelligenceProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, organizationAllowList: OrganizationAllowList, modelValidationError?: string

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\LiteLLM.tsx
**Purpose:** Provides LiteLLM settings, including API key and model configuration.

**Exported Functions:**
- `LiteLLM({ apiConfiguration, setApiConfigurationField, organizationAllowList, modelValidationError }: LiteLLMProps)` → `any`
- `handleMessage(event: MessageEvent<ExtensionMessage>)` → `void`

**Exported Types:**
- `type LiteLLMProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, organizationAllowList: OrganizationAllowList, modelValidationError?: string

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\settings\providers\LMStudio.tsx
**Purpose:** Renders LM Studio settings, including API key and model selection.

**Exported Functions:**
- `LMStudio({ apiConfiguration, setApiConfigurationField }: LMStudioProps)` → `any`

**Exported Types:**
- `type LMStudioProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Mistral.tsx
**Purpose:** Renders Mistral API key input field for provider settings.

**Exported Functions:**
- `Mistral({ apiConfiguration, setApiConfigurationField }: MistralProps)` → `any`

**Exported Types:**
- `type MistralProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Moonshot.tsx
**Purpose:** Renders Moonshot provider settings UI components and handles input changes.

**Exported Functions:**
- `Moonshot({ apiConfiguration, setApiConfigurationField }: MoonshotProps)` → `JSX.Element`

**Exported Types:**
- `type MoonshotProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Ollama.tsx
**Purpose:** Displays and manages Ollama provider settings within the UI.

**Exported Functions:**
- `Ollama({ apiConfiguration, setApiConfigurationField }: OllamaProps)` → `JSX.Element`

**Exported Types:**
- `type OllamaProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/ExtensionMessage`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\OpenAI.tsx
**Purpose:** Renders OpenAI provider settings and handles user input changes.

**Exported Functions:**
- `OpenAI({ apiConfiguration, setApiConfigurationField, selectedModelInfo }: OpenAIProps)` → `JSX.Element`
- `allowedTiers` → `any`

**Exported Types:**
- `type OpenAIProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, selectedModelInfo?: ModelInfo

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\OpenAICompatible.tsx
**Purpose:** Provides the UI for configuring OpenAI compatible provider settings.

**Exported Functions:**
- `OpenAICompatible({ apiConfiguration, setApiConfigurationField, organizationAllowList, modelValidationError }: OpenAICompatibleProps)` → `JSX.Element`

**Exported Types:**
- `type OpenAICompatibleProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, organizationAllowList: OrganizationAllowList, modelValidationError?: string

**Key Imports:** `react`, `react-use`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\settings\providers\OpenRouter.tsx
**Purpose:** Renders OpenRouter settings UI and manages user configuration options.

**Exported Functions:**
- `OpenRouter({ apiConfiguration, setApiConfigurationField, routerModels, uriScheme, fromWelcomeView, organizationAllowList, modelValidationError }: OpenRouterProps)` → `JSX.Element`

**Exported Types:**
- `type OpenRouterProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, selectedModelId: string

**Key Imports:** `react`, `react-i18next`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\settings\providers\OpenRouterBalanceDisplay.tsx
**Purpose:** Displays the OpenRouter API key balance within the settings UI.

**Exported Functions:**
- `OpenRouterBalanceDisplay({ apiKey, baseUrl }: { apiKey: string; baseUrl?: string })` → `JSX.Element`

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@/components/ui/hooks/useOpenRouterKeyInfo`

---

### webview-ui\src\components\settings\providers\QwenCode.tsx
**Purpose:** Provides QwenCode settings UI and handles input/blur events.

**Exported Functions:**
- `handleInputChange(e: Event | React.FormEvent<HTMLElement>)` → `void`
- `handleBlur(e: Event | React.FormEvent<HTMLElement>)` → `void`

**Exported Types:**
- `interface QwenCodeProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\settings\providers\Requesty.tsx
**Purpose:** Renders Requesty provider settings and manages configuration options.

**Exported Functions:**
- `Requesty({ apiConfiguration, setApiConfigurationField, routerModels, refetchRouterModels, organizationAllowList, modelValidationError, uriScheme }: RequestyProps)` → `JSX.Element`
- `getApiKeyUrl` → `string`

**Exported Types:**
- `type RequestyProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, refetchRouterModels: () => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/utils/vscode`

---

### webview-ui\src\components\settings\providers\RequestyBalanceDisplay.tsx
**Purpose:** Displays the Requesty API key balance in the settings UI.

**Exported Functions:**
- `RequestyBalanceDisplay({ baseUrl, apiKey }: RequestyBalanceDisplayProps)` → `JSX.Element`

**Exported Types:**
- `type RequestyBalanceDisplayProps`: apiKey: string, baseUrl?: string

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@/components/ui/hooks/useRequestyKeyInfo`, `@roo/utils/requesty`

---

### webview-ui\src\components\settings\providers\SambaNova.tsx
**Purpose:** Renders SambaNova provider settings and handles input changes.

**Exported Functions:**
- `SambaNova({ apiConfiguration, setApiConfigurationField }: SambaNovaProps)` → `JSX.Element`

**Exported Types:**
- `type SambaNovaProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Unbound.tsx
**Purpose:** Provides the UI for configuring Unbound provider settings.

**Exported Functions:**
- `Unbound({ apiConfiguration, setApiConfigurationField, routerModels, organizationAllowList, modelValidationError }: UnboundProps)` → `JSX.Element`
- `messageHandler` → `any`

**Exported Types:**
- `type UnboundProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings], isUserAction?: boolean,) => void, routerModels?: RouterModels, organizationAllowList: OrganizationAllowList

**Key Imports:** `react`, `react-query`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\VercelAiGateway.tsx
**Purpose:** Renders Vercel AI Gateway settings and handles input changes.

**Exported Functions:**
- `VercelAiGateway({ apiConfiguration, setApiConfigurationField, routerModels, organizationAllowList, modelValidationError }: VercelAiGatewayProps)` → `JSX.Element`

**Exported Types:**
- `type VercelAiGatewayProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, organizationAllowList: OrganizationAllowList

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Vertex.tsx
**Purpose:** Renders Vertex AI provider settings and handles input changes.

**Exported Functions:**
- `Vertex({ apiConfiguration, setApiConfigurationField, fromWelcomeView }: VertexProps)` → `JSX.Element`

**Exported Types:**
- `type VertexProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, fromWelcomeView?: boolean

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\VSCodeLM.tsx
**Purpose:** Displays and manages VSCode Language Model settings in the UI.

**Exported Functions:**
- `VSCodeLM({ apiConfiguration, setApiConfigurationField }: VSCodeLMProps)` → `JSX.Element`

**Exported Types:**
- `type VSCodeLMProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `react-use`, `vscode`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\XAI.tsx
**Purpose:** Renders XAI provider settings and handles input changes.

**Exported Functions:**
- `XAI({ apiConfiguration, setApiConfigurationField }: XAIProps)` → `JSX.Element`

**Exported Types:**
- `type XAIProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\ZAi.tsx
**Purpose:** Renders the ZAi provider settings configuration form.

**Exported Functions:**
- `ZAi({ apiConfiguration, setApiConfigurationField }: ZAiProps)` → `JSX.Element`

**Exported Types:**
- `type ZAiProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\R1FormatSetting.tsx
**Purpose:** Provides a setting to enable or disable R1 format in OpenAI.

**Exported Functions:**
- `R1FormatSetting({ onChange, openAiR1FormatEnabled }: R1FormatSettingProps)` → `JSX.Element`

**Exported Types:**
- `interface R1FormatSettingProps`: onChange: (value: boolean) => void, openAiR1FormatEnabled?: boolean

**Key Imports:** `vscrui`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\RateLimitSecondsControl.tsx
**Purpose:** Renders a slider control for setting rate limit seconds.

**Exported Functions:**
- `RateLimitSecondsControl({ value, onChange }: RateLimitSecondsControlProps)` → `React.FC<RateLimitSecondsControlProps>`

**Exported Types:**
- `interface RateLimitSecondsControlProps`: value: number, onChange: (value: number) => void

**Key Imports:** `react`, `@/components/ui`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\Section.tsx
**Purpose:** Creates a styled section container with padding and gap.

**Exported Functions:**
- `Section({ className, ...props }: SectionProps)` → `JSX.Element`

**Exported Types:**
- `type SectionProps`: className, ...props

**Key Imports:** `react`, `@/lib/utils`

---

### webview-ui\src\components\settings\SectionHeader.tsx
**Purpose:** Renders a sticky section header with title and description.

**Exported Functions:**
- `SectionHeader({ description, children, className, ...props }: SectionHeaderProps)` → `JSX.Element`

**Exported Types:**
- `type SectionHeaderProps`: children: React.ReactNode, description?: string, className, ...props

**Key Imports:** `react`, `@/lib/utils`

---

### webview-ui\src\components\settings\SettingsView.tsx
**Purpose:** Manages the settings view, handling various configurations and UI elements.

**Exported Functions:**
- `handleSubmit` → ``
- `handleMessage` → ``
- `onSelect` → ``
- `triggerComponent` → ``

**Key Imports:** `react`, `lucide-react`, `@roo-code/types`, `@src/utils/vscode`, `@src/lib/utils`

---

### webview-ui\src\components\settings\SlashCommandsSettings.tsx
**Purpose:** Provides settings UI for managing slash commands within the extension.

**Exported Functions:**
- `handleRefresh()` → `void`
- `handleDeleteClick` → ``
- `handleDeleteConfirm` → ``
- `handleDeleteCancel` → ``
- `handleCreateCommand` → ``
- `handleCommandClick` → ``

**Key Imports:** `react`, `lucide-react`, `react-i18next`, `@roo/ExtensionMessage`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\settings\styles.ts
**Purpose:** Defines styled components for the settings view.

**Exported Constants:**
- `StyledMarkdown` = `styled.div`

**Key Imports:** `styled-components`

---

### webview-ui\src\components\settings\TemperatureControl.tsx
**Purpose:** Renders a temperature control with a slider and checkbox.

**Exported Functions:**
- `TemperatureControl({ value, onChange, maxValue = 1 }: TemperatureControlProps)` → `JSX.Element`

**Exported Types:**
- `interface TemperatureControlProps`: value: number | undefined | null, onChange: (value: number | undefined | null) => void, maxValue?: number

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `react`, `@src/i18n/TranslationContext`, `react-use`, `@/components/ui`

---

### webview-ui\src\components\settings\TerminalSettings.tsx
**Purpose:** Provides settings UI for configuring terminal-related features.

**Exported Functions:**
- `TerminalSettingsprops: TerminalSettingsProps` → `JSX.Element`

**Exported Types:**
- `type TerminalSettingsProps`: terminalOutputLineLimit?: number, terminalOutputCharacterLimit?: number, terminalShellIntegrationTimeout?: number, terminalShellIntegrationDisabled?: boolean

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `@src/utils/vscode`, `lucide-react`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\settings\ThinkingBudget.tsx
**Purpose:** Renders a control for setting the thinking budget for models.

**Exported Functions:**
- `ThinkingBudget({ apiConfiguration, setApiConfigurationField, modelInfo }: ThinkingBudgetProps)` → `JSX.Element`

**Exported Types:**
- `interface ThinkingBudgetProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: <K extends keyof ProviderSettings>(field: K, value: ProviderSettings[K], isUserAction?: boolean) => void, modelInfo?: ModelInfo

**Key Imports:** `react`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`, `@src/components/ui`, `@src/components/ui/hooks/useSelectedModel`

---

### webview-ui\src\components\settings\TodoListSettingsControl.tsx
**Purpose:** Provides a control to enable or disable the todo list feature.

**Exported Functions:**
- `TodoListSettingsControl({ todoListEnabled = true, onChange }: TodoListSettingsControlProps)` → `React.FC<TodoListSettingsControlProps>`

**Exported Types:**
- `interface TodoListSettingsControlProps`: todoListEnabled?: boolean, onChange: (field: "todoListEnabled", value: any) => void

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\settings\transforms.ts
**Purpose:** Defines transformation functions for input events.

**Exported Functions:**
- `noTransform<T>(value: T)` → `T`
- `inputEventTransform<E>(event: E)` → `any`

---

### webview-ui\src\components\settings\types.ts
**Purpose:** Defines type definitions for settings-related components.

**Exported Types:**
- `type SetCachedStateField`: field: K, value: ExtensionStateContextType[K]
- `type SetExperimentEnabled`: id: ExperimentId, enabled: boolean

**Key Imports:** `@roo-code/types`, `@/context/ExtensionStateContext`

---

### webview-ui\src\components\settings\UISettings.tsx
**Purpose:** Renders UI settings components, managing collapse state and telemetry.

**Exported Functions:**
- `UISettingsreasoningBlockCollapsed: boolean, setCachedStateField: SetCachedStateField<keyof ExtensionStateContextType>, ...props: UISettingsProps` → `JSX.Element`
- `handleReasoningBlockCollapsedChangevalue: boolean` → `void`

**Exported Types:**
- `interface UISettingsProps`: reasoningBlockCollapsed: boolean, setCachedStateField: SetCachedStateField<keyof ExtensionStateContextType>

**Key Imports:** `react`, `@/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`, `lucide-react`, `@/utils/TelemetryClient`

---

### webview-ui\src\components\settings\utils\__tests__\headers.test.ts
---

### webview-ui\src\components\settings\utils\__tests__\organizationFilters.test.ts
---

### webview-ui\src\components\settings\utils\headers.ts
**Purpose:** Converts an array of headers to a trimmed key-value object.

**Exported Functions:**
- `convertHeadersToObjectheaders: [string, string][]` → `Record<string, string>`

---

### webview-ui\src\components\settings\utils\organizationFilters.ts
**Purpose:** Filters providers and models based on organization allow lists.

**Exported Functions:**
- `filterProvidersproviders: Array<{ value: string; label: string }>, organizationAllowList?: OrganizationAllowList` → `Array<{ value: string; label: string }>`
- `filterModelsmodels: Record<string, ModelInfo> | null, providerId?: ProviderName, organizationAllowList?: OrganizationAllowList` → `Record<string, ModelInfo> | null`

**Key Imports:** `type { ProviderName, ModelInfo, OrganizationAllowList } from "@roo-code/types"`

---

### webview-ui\src\components\settings\Verbosity.tsx
**Purpose:** Displays and manages the verbosity settings for API configurations.

**Exported Functions:**
- `VerbosityapiConfiguration: ProviderSettings, setApiConfigurationField: <K extends keyof ProviderSettings>(field: K, value: ProviderSettings[K]) => void, modelInfo?: ModelInfo` → `JSX.Element | null`

**Exported Types:**
- `interface VerbosityProps`: apiConfiguration: ProviderSettings, setApiConfigurationField, modelInfo?: ModelInfo

**Key Imports:** `type { ProviderSettings, type ModelInfo, type VerbosityLevel, verbosityLevels } from "@roo-code/types"`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\ui\__tests__\select-dropdown.spec.tsx
---

### webview-ui\src\components\ui\__tests__\toggle-switch.spec.tsx
---

### webview-ui\src\components\ui\__tests__\tooltip.spec.tsx
---

### webview-ui\src\components\ui\alert-dialog.tsx
**Purpose:** Provides styled components for creating alert dialogs.

**Exported Functions:**
- `AlertDialog{ ...props }` → ``
- `AlertDialogTrigger{ ...props }` → ``
- `AlertDialogPortal{ ...props }` → ``
- `AlertDialogOverlayclassName, ...props` → ``
- `AlertDialogContentclassName, ...props` → ``
- `AlertDialogHeader{ children }` → ``
- `AlertDialogFooter{ children }` → ``
- `AlertDialogTitle{ children }` → ``
- `AlertDialogDescription{ children }` → ``
- `AlertDialogAction{ children, onClick }` → ``
- `AlertDialogCancel{ children, onClick }` → ``

**Key Imports:** `react`, `@radix-ui/react-alert-dialog`, `@/lib/utils`, `@/components/ui/button`

---

### webview-ui\src\components\ui\autosize-textarea.tsx
**Purpose:** Implements a textarea that automatically adjusts its size.

**Exported Functions:**
- `useAutosizeTextArea{ textAreaRef, triggerAutoSize, maxHeight, minHeight }` → ``

**Exported Types:**
- `interface UseAutosizeTextAreaProps`: textAreaRef, minHeight, maxHeight, triggerAutoSize
- `type AutosizeTextAreaRef`: textArea, maxLength

**Key Imports:** `react`, `@/lib/utils`

---

### webview-ui\src\components\ui\badge.tsx
**Purpose:** Creates styled badge components with various visual states.

**Exported Types:**
- `interface BadgeProps`: className, variant

**Exported Constants:**
- `badgeVariants` = `cva(...)`

**Key Imports:** `react`, `class-variance-authority`, `@/lib/utils`

---

### webview-ui\src\components\ui\button.tsx
**Purpose:** Provides styled button components with different variants.

**Exported Constants:**
- `buttonVariants` = `cva(...)`

**Key Imports:** `react`, `@radix-ui/react-slot`, `class-variance-authority`, `@/lib/utils`

---

### webview-ui\src\components\ui\checkbox.tsx
**Purpose:** Creates a styled checkbox component with various states.

**Exported Types:**
- `interface CheckboxProps`: className, variant

**Exported Constants:**
- `checkboxVariants` = `cva(...)`

**Key Imports:** `react`, `@radix-ui/react-checkbox`, `lucide-react`, `class-variance-authority`, `@/lib/utils`

---

### webview-ui\src\components\ui\collapsible.tsx
**Purpose:** Provides collapsible components for expanding and collapsing content.

**Exported Constants:**
- `Collapsible` = `CollapsiblePrimitive.Root`
- `CollapsibleTrigger` = `CollapsiblePrimitive.CollapsibleTrigger`
- `CollapsibleContent` = `CollapsiblePrimitive.CollapsibleContent`

**Key Imports:** `@radix-ui/react-collapsible`

---

### webview-ui\src\components\ui\command.tsx
**Purpose:** Renders a command palette UI using Radix and cmdk components.

**Exported Functions:**
- `CommandDialog({ children, ...props }: DialogProps)` → `React.ReactElement`
- `CommandInput({ className, ...props }, ref)` → `React.ReactElement`
- `CommandShortcut({ className, ...props }: React.ComponentPropsWithoutRef<typeof CommandPrimitive.Shortcut>)` → `React.ReactElement`

**Exported Types:**
- `class Command`: className, children, ref, props

**Key Imports:** `react`, `@radix-ui/react-dialog`, `cmdk`, `@radix-ui/react-icons`, `@/lib/utils`

---

### webview-ui\src\components\ui\dialog.tsx
**Purpose:** Provides dialog components using Radix UI primitives for UI.

**Exported Functions:**
- `Dialog({ ...props }: React.ComponentProps<typeof DialogPrimitive.Root>)` → `React.ReactElement`
- `DialogTrigger({ ...props }: React.ComponentProps<typeof DialogPrimitive.Trigger>)` → `React.ReactElement`
- `DialogPortal({ ...props }: React.ComponentProps<typeof DialogPrimitive.Portal>)` → `React.ReactElement`
- `DialogClose({ ...props }: React.ComponentProps<typeof DialogPrimitive.Close>)` → `React.ReactElement`
- `DialogOverlay({ className, ...props }: React.ComponentProps<typeof DialogPrimitive.Overlay>)` → `React.ReactElement`
- `DialogContent({ className, children, ...props }: React.ComponentProps<typeof DialogPrimitive.Content>)` → `React.ReactElement`
- `DialogHeader({ className, ...props }: React.ComponentProps<typeof DialogPrimitive.Content>)` → `React.ReactElement`
- `DialogFooter({ className, ...props }: React.ComponentProps<typeof DialogPrimitive.Content>)` → `React.ReactElement`
- `DialogTitle({ className, ...props }: React.ComponentProps<typeof DialogPrimitive.Title>)` → `React.ReactElement`
- `DialogDescription({ className, ...props }: React.ComponentProps<typeof DialogPrimitive.Description>)` → `React.ReactElement`

**Key Imports:** `react`, `@radix-ui/react-dialog`, `lucide-react`, `@/lib/utils`

---

### webview-ui\src\components\ui\dropdown-menu.tsx
**Purpose:** Creates dropdown menu components using Radix UI primitives.

**Exported Functions:**
- `DropdownMenuContent({ className, sideOffset = 4, container, ...props }, ref)` → `React.ReactElement`
- `DropdownMenuShortcut({ className, ...props }: React.ComponentPropsWithoutRef<typeof DropdownMenuPrimitive.Shortcut>)` → `React.ReactElement`

**Exported Types:**
- `class DropdownMenu`: children, props
- `class DropdownMenuTrigger`: children, props
- `class DropdownMenuGroup`: children, props
- `class DropdownMenuPortal`: children, props
- `class DropdownMenuRadioGroup`: children, props

**Key Imports:** `react`, `@radix-ui/react-dropdown-menu`, `@radix-ui/react-portal`, `@radix-ui/react-icons`, `@/lib/utils`

---

### webview-ui\src\components\ui\hooks\__tests__\useSelectedModel.spec.ts
**Functions:** `createWrapper`

---

### webview-ui\src\components\ui\hooks\index.ts
**Purpose:** Exports all hooks from the ui hooks directory.

**Key Imports:** `./useClipboard`, `./useRooPortal`, `./useNonInteractiveClick`

---

### webview-ui\src\components\ui\hooks\useClipboard.ts
**Purpose:** Provides a hook for copying text to the clipboard.

**Exported Functions:**
- `useClipboard({ timeout = 2000 }: UseClipboardProps = {})` → `{ isCopied: boolean; copy: (value: string) => void; }`

**Exported Types:**
- `interface UseClipboardProps`: timeout

**Key Imports:** `react`

---

### webview-ui\src\components\ui\hooks\useLmStudioModels.ts
**Purpose:** Fetches and manages LM Studio models using react-query.

**Exported Functions:**
- `useLmStudioModels(modelId?: string)` → `any`

**Key Imports:** `react-query`, `@roo/api`, `@roo/ExtensionMessage`, `@src/utils/vscode`

---

### webview-ui\src\components\ui\hooks\useNonInteractiveClick.ts
**Purpose:** Adds a click listener for non-interactive elements.

**Exported Functions:**
- `useAddNonInteractiveClickListener(handler: () => void)` → `void`

**Key Imports:** `react`

---

### webview-ui\src\components\ui\hooks\useOllamaModels.ts
**Purpose:** Fetches and manages Ollama models using react-query.

**Exported Functions:**
- `useOllamaModels(modelId?: string)` → `any`

**Key Imports:** `react-query`, `@roo/api`, `@roo/ExtensionMessage`, `@src/utils/vscode`

---

### webview-ui\src\components\ui\hooks\useOpenRouterKeyInfo.ts
**Purpose:** Fetches OpenRouter API key information using react-query.

**Exported Functions:**
- `useOpenRouterKeyInfo(apiKey?: string, baseUrl?: string, options?: UseOpenRouterKeyIn` → `any`

**Exported Types:**
- `type OpenRouterKeyInfo`: label, usage, is_free_tier, is_provisioning_key

**Key Imports:** `axios`, `zod`, `react-query`

---

### webview-ui\src\components\ui\hooks\useOpenRouterModelProviders.ts
**Purpose:** Fetches OpenRouter model providers using react-query.

**Exported Functions:**
- `useOpenRouterModelProviders(modelId: string, apiKey?: string, baseUrl?: string)` → `any`

**Exported Types:**
- `type OpenRouterModelProvider`: label

**Key Imports:** `axios`, `zod`, `react-query`, `@roo-code/types`, `@roo/cost`

---

### webview-ui\src\components\ui\hooks\useRequestyKeyInfo.ts
**Purpose:** Fetches Requesty API key information using react-query.

**Exported Functions:**
- `useRequestyKeyInfo(baseUrl?: string, apiKey?: string, options?: UseRequestyKeyInfoOptions)` → `any`

**Exported Types:**
- `type RequestyKeyInfo`: name, monthly_limit, monthly_spend, org_balance

**Key Imports:** `axios`, `zod`, `react-query`, `@roo/utils/requesty`

---

### webview-ui\src\components\ui\hooks\useRooPortal.ts
**Purpose:** Provides a React portal for a given DOM element ID.

**Exported Functions:**
- `useRooPortal(id: string)` → `HTMLElement | undefined`

**Key Imports:** `react`, `react-use`

---

### webview-ui\src\components\ui\hooks\useRouterModels.ts
**Purpose:** Fetches and manages router models using react-query.

**Exported Functions:**
- `useRouterModels()` → `any`

**Key Imports:** `react-query`, `@roo/api`, `@roo/ExtensionMessage`, `@src/utils/vscode`

---

### webview-ui\src\components\ui\hooks\useSelectedModel.ts
**Purpose:** Selects a model based on provider settings and available models.

**Exported Functions:**
- `useSelectedModel(providerSettings: ProviderSettings, routerModels: RouterModels | undefined, lmStudioModels: ModelRecord | undefined, ollamaModels: ModelRecord | undefined, openRouterProviders: OpenRouterModelProvider[] | undefined, requestyKeyInfo: RequestyKeyInfo | null, openRouterKeyInfo: OpenRouterKeyInfo | null)` → `any`

**Key Imports:** `@roo-code/types`, `@roo/api`, `./useRouterModels`, `./useOpenRouterKeyInfo`

---

### webview-ui\src\components\ui\index.ts
**Purpose:** Exports UI components for use in the application.

**Key Imports:** `./alert-dialog`, `./autosize-textarea`, `./badge`, `./button`, `./checkbox`

---

### webview-ui\src\components\ui\input.tsx
**Purpose:** Creates a styled input component using React.

**Exported Types:**
- `class Input`: className, type, ref, props

**Key Imports:** `react`, `@/lib/utils`

---

### webview-ui\src\components\ui\popover.tsx
**Purpose:** Creates popover components using Radix UI primitives.

**Exported Types:**
- `class Popover`: children, props
- `class PopoverTrigger`: children, props
- `class PopoverContent`: className, align, sideOffset, container, props
- `class PopoverAnchor`: children, props

**Key Imports:** `react`, `@radix-ui/react-portal`, `@radix-ui/react-popover`, `@/lib/utils`

---

### webview-ui\src\components\ui\progress.tsx
**Purpose:** Creates a progress bar component using Radix UI.

**Exported Types:**
- `class Progress`: className, value, props

**Key Imports:** `react`, `@radix-ui/react-progress`, `@/lib/utils`

---

### webview-ui\src\components\ui\searchable-select.tsx
**Purpose:** Creates a searchable select component with options and search functionality.

**Exported Functions:**
- `SearchableSelect({
	value,
	onValueChange,
	options,
	placeholder,
	searchPlaceholder,
	emptyMessage,
	className,
	disabled,
	"data-testid": dataTestId,
}: SearchableSelectProps)` → `React.ReactElement`

**Exported Types:**
- `interface SearchableSelectOption`: value: string, label: string, disabled?: boolean, icon?: React.ReactNode
- `interface SearchableSelectProps`: value?: string, onValueChange: (value: string) => void, options: SearchableSelectOption[], placeholder: string

**Key Imports:** `react`, `lucide-react`, `cn`, `Button`, `Command`

---

### webview-ui\src\components\ui\select-dropdown.tsx
**Purpose:** Provides a customizable dropdown component for selecting options.

**Exported Types:**
- `enum DropdownOptionType`: ITEM = "item", SEPARATOR = "separator", SHORTCUT = "shortcut", ACTION = "action"
- `interface DropdownOption`: value: string, label: string, disabled?: boolean, type?: DropdownOptionType
- `interface SelectDropdownProps`: value: string, options: DropdownOption[], onChange: (value: string) => void, disabled?: boolean

**Key Imports:** `react`, `react-icons`, `lucide-react`, `Fzf`, `react-i18next`

---

### webview-ui\src\components\ui\select.tsx
**Purpose:** Implements a customizable select component using Radix UI primitives.

**Exported Functions:**
- `Select{ ...props }: React.ComponentProps<typeof SelectPrimitive.Root>` → `React.ReactElement`
- `SelectGroup{ ...props }: React.ComponentProps<typeof SelectPrimitive.Group>` → `React.ReactElement`
- `SelectValue{ ...props }: React.ComponentProps<typeof SelectPrimitive.Value>` → `React.ReactElement`
- `SelectTrigger{ className, children, ...props }: React.ComponentProps<typeof SelectPrimitive.Trigger>` → `React.ReactElement`
- `SelectContent{ children, position, className, ...props }: React.ComponentProps<typeof SelectPrimitive.Content>` → `React.ReactElement`
- `SelectLabel{ className, ...props }: React.ComponentProps<typeof SelectPrimitive.Label>` → `React.ReactElement`
- `SelectItem{ className, children, ...props }: React.ComponentProps<typeof SelectPrimitive.Item>` → `React.ReactElement`
- `SelectSeparator{ ...props }: React.ComponentProps<typeof SelectPrimitive.Separator>` → `React.ReactElement`
- `SelectScrollUpButton{ ...props }: React.ComponentProps<typeof SelectPrimitive.ScrollUpButton>` → `React.ReactElement`
- `SelectScrollDownButton{ ...props }: React.ComponentProps<typeof SelectPrimitive.ScrollDownButton>` → `React.ReactElement`

**Key Imports:** `react`, `react-portal`, `react-select`, `lucide-react`, `cn`

---

### webview-ui\src\components\ui\separator.tsx
**Purpose:** Creates a separator component for visual separation in UI.

**Exported Functions:**
- `Separator({ className, orientation = "horizontal", decorative = true, ...props }, ref)` → `React.ReactElement`

**Key Imports:** `react`, `react-separator`, `cn`

---

### webview-ui\src\components\ui\slider.tsx
**Purpose:** Provides a slider component for selecting a numerical value.

**Exported Functions:**
- `Slider({ className, ...props }, ref)` → `React.ReactElement`

**Key Imports:** `react`, `react-slider`, `cn`

---

### webview-ui\src\components\ui\standard-tooltip.tsx
**Purpose:** Implements a standard tooltip component with a consistent delay.

**Exported Functions:**
- `StandardTooltipprops: StandardTooltipProps` → `React.ReactElement`

**Exported Types:**
- `interface StandardTooltipProps`: children: ReactNode, content: ReactNode, side?: "top" | "right" | "bottom" | "left", align?: "start" | "center" | "end"

**Exported Constants:**
- `STANDARD_TOOLTIP_DELAY` = `300`

**Key Imports:** `react`, `Tooltip`, `TooltipContent`, `TooltipTrigger`

---

### webview-ui\src\components\ui\textarea.tsx
**Purpose:** Creates a styled textarea component for multi-line text input.

**Exported Functions:**
- `Textarea({ className, ...props }, ref)` → `React.ReactElement`

**Key Imports:** `react`, `cn`

---

### webview-ui\src\components\ui\toggle-switch.tsx
**Purpose:** Provides a toggle switch component for boolean state control.

**Exported Functions:**
- `ToggleSwitch{
	checked,
	onChange,
	disabled = false,
	size = "small",
	"aria-label": ariaLabel,
	"data-testid": dataTestId,
}` → `React.ReactElement`

**Exported Types:**
- `interface ToggleSwitchProps`: checked: boolean, onChange: () => void, disabled?: boolean, size?: "small" | "medium"

**Key Imports:** `react`

---

### webview-ui\src\components\ui\tooltip.tsx
**Purpose:** Implements tooltip components using Radix UI primitives.

**Exported Functions:**
- `TooltipProvider{ delayDuration = 0, ...props }: React.ComponentProps<typeof TooltipPrimitive.Provider>` → `React.ReactElement`
- `Tooltip{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Root>` → `React.ReactElement`
- `TooltipTrigger{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Trigger>` → `React.ReactElement`
- `TooltipContent{
	className,
	sideOffset = 0,
	children,
	...props
}: React.ComponentProps<typeof TooltipPrimitive.Content>` → `React.ReactElement`

**Key Imports:** `react`, `react-tooltip`, `cn`

---

### webview-ui\src\components\welcome\__tests__\RooTips.spec.tsx
---

### webview-ui\src\components\welcome\RooHero.tsx
**Purpose:** Displays the Roo logo in a welcome screen hero section.

**Exported Functions:**
- `RooHero()` → `React.ReactElement`

**Key Imports:** `useState`

---

### webview-ui\src\components\welcome\RooTips.tsx
**Purpose:** Renders helpful tips for using the Roo extension.

**Exported Functions:**
- `RooTips()` → `React.ReactElement`

**Key Imports:** `VSCodeLink`, `react-i18next`, `Trans`, `buildDocLink`

---

### webview-ui\src\components\welcome\WelcomeView.tsx
**Purpose:** Provides the main welcome view for the Roo extension.

**Exported Functions:**
- `WelcomeView()` → `React.ReactElement`
- `onFeatureFlags` → ``

**Key Imports:** `useCallback`, `useState`, `useEffect`, `knuthShuffle`, `Trans`

---

### webview-ui\src\context\__tests__\ExtensionStateContext.spec.tsx
**Purpose:** Tests the ExtensionStateContext's state management and updates.

**Key Imports:** `@`, `@roo-code/types`, `@roo/ExtensionMessage`, `../ExtensionStateContext`

---

### webview-ui\src\context\ExtensionStateContext.tsx
**Purpose:** Manages and provides the application's extension state context.

**Exported Types:**
- `interface ExtensionStateContextType`: historyPreviewCollapsed?, didHydrateState, showWelcome, theme, mcpServers

**Key Imports:** `react`, `@roo-code/types`, `@roo/ExtensionMessage`, `@roo/array`, `@roo/mcp`

---

### webview-ui\src\hooks\__tests__\useAutoApprovalState.spec.ts
**Purpose:** Tests the useAutoApprovalState hook's logic and return values.

**Key Imports:** `@testing-library/react`, `../useAutoApprovalState`

---

### webview-ui\src\hooks\useAutoApprovalState.ts
**Purpose:** Provides auto-approval state based on toggle configurations.

**Exported Functions:**
- `useAutoApprovalState(toggles: AutoApprovalToggles, autoApprovalEnabled?: boolean)` → `{ hasEnabledOptions; effectiveAutoApprovalEnabled; }`

**Exported Types:**
- `interface AutoApprovalToggles`: alwaysAllowReadOnly?, alwaysAllowWrite?, alwaysAllowExecute?, alwaysAllowBrowser?, alwaysAllowMcp?

**Key Imports:** `react`

---

### webview-ui\src\hooks\useAutoApprovalToggles.ts
**Purpose:** Creates and returns auto-approval toggles from extension state.

**Exported Functions:**
- `useAutoApprovalToggles()` → `any`

**Key Imports:** `react`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\hooks\useCloudUpsell.ts
**Purpose:** Manages the cloud upsell dialog's authentication and display logic.

**Exported Functions:**
- `useCloudUpsell(options: UseCloudUpsellOptions = {})` → `any`

**Exported Types:**
- `interface UseCloudUpsellOptions`: onAuthSuccess?, autoOpenOnAuth?

**Key Imports:** `react`, `@roo-code/types`, `@/utils/vscode`, `@/utils/TelemetryClient`, `@/context/ExtensionStateContext`

---

### webview-ui\src\hooks\useEscapeKey.spec.ts
**Purpose:** Tests the useEscapeKey hook's functionality and event handling.

**Key Imports:** `@testing-library/react`, `./useEscapeKey`

---

### webview-ui\src\hooks\useEscapeKey.ts
**Purpose:** Handles ESC key press events within a React component.

**Exported Functions:**
- `useEscapeKey(isOpen: boolean, onEscape: () => void, options: { preventDefault?: boolean; stopPropagation?: boolean; } = {})` → `void`

**Key Imports:** `react`

---

### webview-ui\src\i18n\__mocks__\TranslationContext.tsx
**Purpose:** Mocks the TranslationContext for testing purposes.

**Exported Functions:**
- `useAppTranslation` → `any`

**Exported Constants:**
- `TranslationContext` = `any`

**Key Imports:** `react`

---

### webview-ui\src\i18n\__tests__\TranslationContext.spec.tsx
**Purpose:** Tests the TranslationContext and its translation functionality.

**Key Imports:** `@/utils/test-utils`, `../TranslationContext`

---

### webview-ui\src\i18n\setup.ts
**Purpose:** Dynamically loads and initializes i18next translations for the app.

**Exported Functions:**
- `loadTranslations()` → `void`

**Key Imports:** `i18next`, `react-i18next`

---

### webview-ui\src\i18n\TranslationContext.tsx
**Purpose:** Provides a React context for managing application translations.

**Exported Functions:**
- `useAppTranslation` → `any`

**Exported Types:**
- `type TranslationProvider`: children

**Exported Constants:**
- `TranslationContext` = `any`

**Key Imports:** `react`, `react-i18next`, `./setup`, `@/context/ExtensionStateContext`

---

### webview-ui\src\index.tsx
**Purpose:** Renders the main application component into the DOM.

**Key Imports:** `react`, `react-dom/client`, `./index.css`, `./App`, `../node_modules/@vscode/codicons/dist/codicon.css`, `./utils/highlighter`

---

### webview-ui\src\lib\utils.ts
**Purpose:** Provides utility functions for common tasks.

**Exported Functions:**
- `cn(...inputs: ClassValue[])` → `string`

**Key Imports:** `clsx`, `tailwind-merge`

---

### webview-ui\src\oauth\urls.ts
**Purpose:** Generates OAuth authorization URLs for various providers.

**Exported Functions:**
- `getCallbackUrl(provider: string, uriScheme?: string)` → `string`
- `getGlamaAuthUrl(uriScheme?: string)` → `string`
- `getOpenRouterAuthUrl(uriScheme?: string)` → `string`
- `getRequestyAuthUrl(uriScheme?: string)` → `string`

**Key Imports:** `@roo/package`

---

### webview-ui\src\types.d.ts
**Purpose:** Declares types for third-party modules used in the project.

---

### webview-ui\src\utils\__tests__\command-parser.spec.ts
---

### webview-ui\src\utils\__tests__\command-validation.spec.ts
---

### webview-ui\src\utils\__tests__\context-mentions.spec.ts
---

### webview-ui\src\utils\__tests__\format.spec.ts
---

### webview-ui\src\utils\__tests__\model-utils.spec.ts
---

### webview-ui\src\utils\__tests__\path-mentions.test.ts
---

### webview-ui\src\utils\__tests__\sourceMapUtils.spec.ts
**Functions:** `test`

---

### webview-ui\src\utils\__tests__\TelemetryClient.spec.ts
---

### webview-ui\src\utils\__tests__\validate.test.ts
---

### webview-ui\src\utils\clipboard.ts
**Purpose:** Provides functions for copying text to the clipboard.

**Exported Functions:**
- `copyToClipboard(text: string, options?: CopyOptions)` → `Promise<boolean>`
- `useCopyToClipboard(feedbackDuration = 2000)` → `any`

**Exported Types:**
- `interface CopyOptions`: feedbackDuration?, onSuccess?, onError?

**Key Imports:** `react`

---

### webview-ui\src\utils\command-parser.ts
**Purpose:** Extracts command patterns from a given command string.

**Exported Functions:**
- `extractPatternsFromCommandcommand: string` → `string[]`

**Key Imports:** `shell-quote`

---

### webview-ui\src\utils\command-validation.ts
**Purpose:** Validates commands using longest prefix match for allow/denylists.

**Exported Types:**
- `type ShellToken`: string | { op: string } | { command: string }

**Key Imports:** `shell-quote`

---

### webview-ui\src\utils\context-mentions.ts
**Purpose:** Manages context menu options and inserts mentions in text.

**Exported Types:**
- `interface SearchResult`: path: string, type: "file" | "folder", label?: string

**Key Imports:** `fzf`, `@roo-code/types`, `@roo/ExtensionMessage`, `@roo/context-mentions`, `./path-mentions`

---

### webview-ui\src\utils\docLinks.ts
**Purpose:** Builds Roo Code documentation links with UTM telemetry parameters.

**Exported Functions:**
- `buildDocLinkpath: string, campaign: string` → `string`

---

### webview-ui\src\utils\format.ts
**Purpose:** Formats large numbers, dates, and time ago strings.

**Exported Functions:**
- `formatLargeNumbernum: number` → `string`
- `formatDatetimestamp: number` → `any`
- `formatTimeAgotimestamp: number` → `any`

**Key Imports:** `i18next`

---

### webview-ui\src\utils\formatPrice.ts
**Purpose:** Formats a number as a currency price in USD.

**Exported Functions:**
- `formatPriceprice: number` → `any`

---

### webview-ui\src\utils\getLanguageFromPath.ts
**Purpose:** Determines the programming language from a file path.

**Exported Functions:**
- `getLanguageFromPathpath: string` → `string | undefined`

---

### webview-ui\src\utils\highlight.ts
**Purpose:** Highlights FZF matches in text using specified positions.

**Exported Functions:**
- `highlightFzfMatchtext: string, positions: number[], highlightClassName: string = "history-item-highlight"` → `any`

**Key Imports:** `lru-cache`

---

### webview-ui\src\utils\highlighter.ts
**Purpose:** Provides utilities for code highlighting using Shiki library.

**Exported Types:**
- `type ExtendedLanguage`: BundledLanguage | "txt"

**Key Imports:** `shiki`

---

### webview-ui\src\utils\imageUtils.ts
**Purpose:** Appends new images to an array, respecting a maximum limit.

**Exported Functions:**
- `appendImagescurrentImages: string[], newImages: string[] | undefined, maxImages: number` → `string[]`

---

### webview-ui\src\utils\mcp.ts
**Purpose:** Finds matching MCP templates or resources by URI matching.

**Exported Functions:**
- `findMatchingTemplateuri: string, templates: McpResourceTemplate[] = []` → `McpResourceTemplate | undefined`
- `findMatchingResourceOrTemplateuri: string, resources: McpResource[] = [], templates: McpResourceTemplate[] = []` → `McpResource | McpResourceTemplate | undefined`

**Key Imports:** `@roo/mcp`

---

### webview-ui\src\utils\model-utils.ts
**Purpose:** Calculates and visualizes token distribution within a context window.

**Exported Types:**
- `interface TokenDistributionResult`: currentPercent: number, reservedPercent: number, availablePercent: number, reservedForOutput: number, availableSize: number

**Key Imports:** `@roo-code/types`

---

### webview-ui\src\utils\path-mentions.ts
**Purpose:** Provides utilities for handling path-related operations in mentions.

**Exported Functions:**
- `escapeSpacespath: string` → `string`
- `convertToMentionPathpath: string, cwd?: string` → `string`

---

### webview-ui\src\utils\removeLeadingNonAlphanumeric.ts
**Purpose:** Removes leading non-alphanumeric characters from a path string.

**Exported Functions:**
- `removeLeadingNonAlphanumericpath: string` → `string`

---

### webview-ui\src\utils\sourceMapInitializer.ts
**Purpose:** Initializes source map support for production builds.

**Exported Functions:**
- `initializeSourceMapsvoid` → `void`

**Key Imports:** `./sourceMapUtils`

---

### webview-ui\src\utils\sourceMapUtils.ts
**Purpose:** Applies source maps to stack traces for enhanced error reporting.

**Exported Types:**
- `interface EnhancedError`: sourceMappedStack?: string, sourceMappedComponentStack?: string

**Key Imports:** `stacktrace-js`

---

### webview-ui\src\utils\TelemetryClient.ts
**Purpose:** Manages and captures telemetry events using PostHog.

**Exported Constants:**
- `telemetryClient` = `TelemetryClient.getInstance()`

**Key Imports:** `posthog-js`, `@roo-code/types`

---

### webview-ui\src\utils\test-utils.tsx
**Purpose:** Provides testing utilities, including a provider wrapper and render override.

**Exported Functions:**
- `AllTheProviders({ children }: AllTheProvidersProps)` → `React.ReactElement`
- `customRender(ui: React.ReactElement, options?: Omit<RenderOptions, "wrapper">)` → `RenderResult`

**Exported Types:**
- `interface AllTheProvidersProps`: children: React.ReactNode

**Key Imports:** `react`, `@testing-library/react`, `@src/components/ui/tooltip`, `@src/components/ui/standard-tooltip`

---

### webview-ui\src\utils\textMateToHljs.ts
**Purpose:** Converts TextMate themes to Highlight.js themes for syntax highlighting.

**Exported Functions:**
- `constructTheme(theme: TextMateTheme, options?: ConstructThemeOptions)` → `HljsTheme`
- `fallbackTheme(theme: TextMateTheme, options?: ConstructThemeOptions)` → `HljsTheme`
- `convertTextMateToHljs(textMateTheme: TextMateTheme, options?: ConvertOptions)` → `HljsTheme`
- `parseHexColor(hex: string)` → `string | undefined`

---

### webview-ui\src\utils\url.ts
**Purpose:** Validates if a given string is a valid URL.

**Exported Functions:**
- `isValidUrl(urlString: string)` → `boolean`

---

### webview-ui\src\utils\useDebounceEffect.ts
**Purpose:** Debounces a React effect, running after a delay when dependencies change.

**Exported Functions:**
- `useDebounceEffect(effect: VoidFn, delay: number, deps: any[])` → `void`

**Exported Types:**
- `type VoidFn`

**Key Imports:** `react`, `useEffect`, `useRef`

---

### webview-ui\src\utils\validate.ts
**Purpose:** Validates API configurations against various criteria and settings.

**Exported Functions:**
- `validateApiConfiguration(apiConfiguration: ProviderSettings, routerModels?: RouterModels, organizationAllowList?: OrganizationAllowList)` → `string | undefined`
- `validateModelsAndKeysProvided(apiConfiguration: ProviderSettings)` → `string | undefined`
- `validateProviderAgainstOrganizationSettings(apiConfiguration: ProviderSettings, organizationAllowList?: OrganizationAllowList)` → `string | undefined`
- `getModelIdForProvider(apiConfiguration: ProviderSettings)` → `string | undefined`
- `validateBedrockArn(arn: string)` → `boolean`
- `validateDynamicProviderModelId(apiConfiguration: ProviderSettings, routerModels?: RouterModels)` → `string | undefined`
- `getModelValidationError(apiConfiguration: ProviderSettings, routerModels?: RouterModels)` → `string | undefined`
- `validateApiConfigurationExcludingModelErrors(apiConfiguration: ProviderSettings, organizationAllowList?: OrganizationAllowList)` → `string | undefined`

**Exported Types:**
- `type ProviderSettings`
- `type OrganizationAllowList`
- `type ProviderName`
- `type RouterModels`

**Key Imports:** `i18next`, `@roo-code/types`, `@roo/api`

---

### webview-ui\src\utils\vscode.ts
**Purpose:** Provides a wrapper for VS Code's webview API for message passing.

**Exported Functions:**
- `constructor()` → `void`
- `postMessage(message: WebviewMessage)` → `void`

**Exported Types:**
- `class VSCodeAPIWrapper`: vsCodeApi: WebviewApi<unknown> | undefined, constructor(): void, postMessage(message: WebviewMessage): void

**Key Imports:** `vscode-webview`, `@roo/WebviewMessage`

---

### webview-ui\src\vite-env.d.ts
---

### webview-ui\src\vite-plugins\sourcemapPlugin.ts
**Purpose:** Ensures source maps are included in the build for debugging.

**Exported Functions:**
- `sourcemapPlugin()` → `Plugin`

**Key Imports:** `vite`, `fs`, `path`

---

### webview-ui\vite.config.ts
**Purpose:** Configures Vite for the webview UI, including plugins and build settings.

**Exported Functions:**
- `getGitSha` → `string | undefined`
- `loadid: any` → `any`
- `configureServerviteDevServer: any` → `any`

**Key Imports:** `path`, `fs`, `child_process`, `vite`, `@vitejs/plugin-react`, `@tailwindcss/vite`

---

### webview-ui\vitest.config.ts
**Purpose:** Configures Vitest for testing the webview UI components.

**Key Imports:** `vitest/config`, `path`, `../src/utils/vitest-verbosity`

---

### webview-ui\vitest.setup.ts
**Purpose:** Sets up Vitest environment and mocks for testing the webview UI.

**Key Imports:** `@testing-library/jest-dom`, `@testing-library/jest-dom/vitest`

---

